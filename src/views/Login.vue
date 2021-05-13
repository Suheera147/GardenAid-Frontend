<template>
  <div class="container-fluid login-container">
    <div class="card form-card">
      <div class="card-header logo">
        <img
          alt="garden-aid logo"
          class="logo-img"
          src="../assets/garden-aid.png"
        />
      </div>
      <div class="card-body welcome-text">
        <p class="welcome">Welcome Back!</p>
        <form class="form-container">
          <div class="form-group">
            <div for="exampleInputEmail1" class="text-left input-labels">
              Email address
            </div>
            <input
              type="email"
              class="form-control"
              id="exampleInputEmail1"
              aria-describedby="emailHelp"
              placeholder="Enter email"
              v-model="email"
            />
          </div>
          <div class="form-group">
            <div for="exampleInputPassword1" class="text-left password">
              Password
            </div>
            <div for="exampleInputPassword1" class="text-right password">
              <small class="forgotpassword">forgot your password?</small>
            </div>
            <input
              type="password"
              v-model="password"
              class="form-control"
              id="exampleInputPassword1"
              placeholder="Password"
            />
          </div>
          <button
            type="button"
            v-on:click="onClickLogin()"
            class="btn btn-primary btn-submit"
          >
            Login
          </button>
        </form>

        <div class="signup-div">
          <router-link to="/signup">
            <a href="#" class="signup-link"> Don't have an account? </a>
          </router-link>
        </div>
      </div>
    </div>
    <div class="card picture-card">
      <img alt="garden-image" class="garden-img" src="../assets/garden.png" />
    </div>
  </div>
</template>

<script>
import axios from "axios";
// @ is an alias to /src

export default {
  name: "Login",

  data() {
    return {
      email: "",
      password: "",
    };
  },

  methods: {
    onClickLogin() {
      var reqbody = new FormData();

      reqbody.append("email", this.email);
      reqbody.append("password", this.password);

      axios
        .post("https://fierce-citadel-60073.herokuapp.com/user/signin", reqbody)
        .then((response) => {
          if (response.status == 202) {
            localStorage.setItem("id", response.data.id);
            localStorage.setItem("name", response.data.name);
            localStorage.setItem("email", response.data.email);
            localStorage.setItem("number", response.data.number);
            this.$router.push("/home");
          }
        });
    },
  },
};
</script>

<style scoped>
.login-container {
  background-color: #023436;
  width: 100vw;
  height: 100vh;
  align-items: center;
  padding-top: 10vh;
  padding-bottom: 10vh;
  padding-right: 12vw;
  padding-left: 12vw;
  margin: 0%;
  margin-right: 0;
}

.form-card {
  background-color: white;
  display: inline-block;
  width: 38vw;
  height: 80vh;
}

@media screen and (max-width: 2200px) {
  .form-card {
    width: 32vw;
  }

  .picture-card {
    width: 32vw;
  }

  .login-container {
    padding-top: 10vh;
    padding-bottom: 10vh;
    padding-right: 18vw;
    padding-left: 18vw;
  }
}

@media screen and (max-width: 1400px) {
  .form-card {
    width: 33vw;
  }

  .picture-card {
    width: 33vw;
  }

  .login-container {
    padding-top: 10vh;
    padding-bottom: 10vh;
    padding-right: 16vw;
    padding-left: 16vw;
  }
}

@media screen and (max-width: 1170px) {
  .picture-card {
    visibility: hidden;
    display: none;
  }

  .garden-img {
    visibility: hidden;
    display: none;
  }

  .form-card {
    width: 33vw;
    min-width: 1rem;
  }

  .form-container {
    min-width: 100px;
    padding-right: 3.5rem;
    padding-left: 3.5rem;
  }
}

@media screen and (max-width: 1000px) {
  .form-card {
    width: 98%;
  }

  .login-container {
    padding-top: 4rem;
    padding-bottom: 1rem;
    padding-right: 1%;
    padding-left: 1%;
    height: 100vh;
  }

  .form-container {
    padding-right: 1rem;
    padding-left: 1rem;
  }
}

.picture-card {
  background-color: green;
  display: inline-block;
  height: 80vh;
}

.card-header {
  border: transparent;
}

.logo {
  position: absolute;
  background-color: white;
}

.logo-img {
  width: 30%;
}

.garden-img {
  position: absolute;
  width: 100%;
  height: 100%;
}

.welcome-text {
  position: absolute;
  margin-top: 5rem;
  text-align: center;
  width: 100%;
}

.welcome {
  font-family: "Molengo";
  font-size: 2.5rem;
  color: #69747c;
}

.form-container {
  position: relative;
  padding-top: 4rem;
}

.input-labels {
  font-family: "Molengo";
}

.btn-submit {
  margin-top: 1.25rem;
  background-color: #6baa75;
  border: #6baa75;
  width: 100%;
}

.password {
  display: inline-block;
  width: 50%;
  font-family: "Molengo";
}

.forgotpassword {
  font-family: "Molengo";
}

.signup-div {
  padding-top: 1.5rem;
  font-family: "Molengo";
}

.signup-link {
  color: #6baa75;
  text-decoration: underline;
}
</style>
