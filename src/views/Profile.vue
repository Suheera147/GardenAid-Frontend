<template>
  <div class="bg-color container-fluid">
    <link
      rel="stylesheet"
      href="https://pro.fontawesome.com/releases/v5.10.0/css/all.css"
      integrity="sha384-AYmEC3Yw5cVb3ZcuHtOA93w35dYTsvhLPVnYs9eStHfGJvOvKxVfELGroGkvsg+p"
      crossorigin="anonymous"
    />
    <nav class="navbar navbar-expand-lg navbar-light navbar-background">
      <a class="navbar-brand" href="#">
        <img
          alt="garden-aid logo"
          class="logo-img navbar-brand"
          src="../assets/garden-aid.png"
        />
      </a>

      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <form class="form-inline my-2 my-lg-0">
        <input
          class="form-control ml-sm-2 search-bar"
          type="search"
          placeholder="Search"
          aria-label="Search"
        />
      </form>

      <div
        class="collapse navbar-collapse nav-items-div"
        id="navbarSupportedContent"
      >
        <ul class="navbar-nav ml-auto">
          <li class="nav-item">
            <a class="nav-link" href="/home">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">About</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Contact</a>
          </li>
          <li class="nav-item">
            <a class="nav-link active" href="#">My Profile</a>
          </li>
          <li class="nav-item">
            <button class="btn btn-primary">
                My Cart
            </button>
          </li>
          <li>
            <button class="btn btn-danger" v-on:click="logout()">
                Logout
                <i class="fas fa-sign-out-alt"></i>
            </button>
          </li>
              
        </ul>
      </div>
    </nav>

    <div class = "image-text">
          <div class = "text-details">
                <h2 class="welcome-text">
                    Hello {{name}} !
                </h2>

                <div class="under-details">
                    <div class="manage-text">
                        <h2 class="manage">
                            MANAGE MY ACCOUNT
                        </h2>
                    </div>

                    <div class="notifications">
                        <div class="notification-text">
                            <i class="far fa-bell"></i>
                            You have 3 Pending Alerts!
                        </div>

                        <div class= "my-plants">
                            <a href="/my-plants" class="plant-link">
                                Go to My Plants
                            </a>
                            
                        </div>
                    </div>
                </div>
          </div>

      <div class="profile-image">
        <img
          alt="garden-aid logo"
          class="profile-img"
          src="../assets/dummy.png"
        />
      </div>
    </div>

    <div class="sidebar-details">
        <div class="side-bar">
            <button type="button" class="btn sidebar-item text-left active-item">
                My Profile
                <pre class="tab">&nbsp;&nbsp;&nbsp;&nbsp;&emsp;</pre>
                <i class="fas fa-arrow-circle-right"></i>
                <hr class="item-divider text-left">
            </button>
            <button type="button" class="btn sidebar-item text-left inactive" v-on:click="goToPlants()">
                My Plants
                <pre class="tab">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</pre>
                <i class="fas fa-arrow-circle-right"></i>
                <hr class="item-divider text-left">
            </button>
            <button type="button" class="btn sidebar-item text-left inactive">
                My Address
                <pre class="tab">&nbsp;&nbsp;&nbsp;&nbsp;</pre>
                <i class="fas fa-arrow-circle-right"></i>
                <hr class="item-divider text-left">
            </button>
            <button type="button" class="btn sidebar-item text-left inactive" v-on:click="goToOrders()">
                My Orders
                <pre class="tab">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</pre>
                <i class="fas fa-arrow-circle-right text-right"></i>
                <hr class="item-divider text-left">
            </button>
            <button type="button" class="btn sidebar-item text-left inactive">
                My Reviews
                <pre class="tab">&nbsp;&nbsp;&nbsp;&nbsp;</pre>
                <i class="fas fa-arrow-circle-right"></i>
                <hr class="item-divider text-left">
            </button>
            <button type="button" class="btn sidebar-item text-left inactive">
                My Favourites
                <pre class="tab">&nbsp;&nbsp;</pre>
                <i class="fas fa-arrow-circle-right"></i>
                <hr class="item-divider text-left">
            </button>
            
        </div>
        <div class="user-details">
            <div class="card user-card">
                <h3 class="detail-item">
                    {{name}}
                </h3>
                <h3 class="detail-item" >
                    {{number}}
                </h3>
                <h3 class="detail-item">
                    {{email}}
                </h3>
            </div>
        </div>
      </div>
    </div>



  
</template>

<script>
export default {
  name: "Profile",

    data() {
        return {
            name: localStorage.getItem('name'),
            email: localStorage.getItem('email'),
            number: localStorage.getItem('number'),
        };
  },

    methods: {
        goToOrders() {
            this.$router.push("/profile/orders")
        },

        logout() {
            localStorage.removeItem('id');
            localStorage.removeItem('number');
            localStorage.removeItem('name');
            localStorage.removeItem('email')
            this.$router.push("/login");
        },
        goToPlants() {
          this.$router.push("/profile/plants");
        },

        goToProfile() {
            this.$router.push("/profile")
        },
    },

};
</script>

<style scoped>

.bg-color {
  background-color: #DAE0DB;
}
.navbar-background {
  background-color: white;
}

.logo-img {
  width: 80%;
  height: 80%;
}

.nav-items-div {
  margin-top: 2rem;
  margin-right: 6rem;
}

.search-bar {
  margin-top: 2rem;
  width: 25rem;
}

.nav-link {
  color: #023436 !important;
  font-weight: 600;
  margin-left: 2rem;
}

.nav-link:hover {
  text-decoration: underline;
}

.active {
  border-radius: 2rem;
  margin-left: 2rem !important;
  text-decoration: underline;
  font-weight: 650;
}

.image-text {
  display: inline-block;
  width: 100%;
  margin-top: 5%;
}

.profile-image {
  margin-left: 20%;
  display: inline-block;
  width: 10%;
  padding-bottom: 13%;
}

.text-details {
  margin-left: 20%;
  display: inline-block;
}

.welcome-text {
  width: 100%;
  margin-block-end: 0%;
  font-size: 300%;
  color: #023436;
}

.profile-img {
  position: absolute;
  display: inline-block;
  width: 28%;
}

.manage-text {
  margin-top: 10%;
  margin-bottom: -20%;
  margin-left: -60%;
  width: 80%;
}

.manage {
  color: #023436;
  font-size: 1.5rem;
}

.under-details {
}

.container-fluid {
    width: 100vw;
    
}
.profile-page {
    background-color: #DAE0DB;
}

 .navbar-background{
    background-color:#DAE0DB;
  }

  .logo-img {
    width: 80%;
    height: 80%;
  }

  .nav-items-div {
    margin-top: 2rem;
    margin-right: 6rem;
  }

  .search-bar {
    margin-top:2rem;
    width: 25rem;
  }

  .nav-link {
    color: #023436 !important;
    font-weight: 600;
    margin-left: 2rem;
  }

  .btn-primary {
      margin-left: 2rem;
      background-color: #023436;
      border: none;
      width: 7rem;
  }

  .btn-danger {
    margin-left: 2rem;
    background-color: #5B3B19;
    border: none;
    width: 7rem;
  }

  .nav-link:hover {
     text-decoration: underline;
  }

  .active {
    border-radius: 2rem;
    margin-left: 2rem !important;
    text-decoration: underline;
    font-weight: 650;
  }

  .image-text {
      display: inline-block;
      width: 100%;
      margin-top: 3rem;
  }

  .profile-image {
      margin-left: 30%;
      display: inline-block;
      width: 10%;
      padding-bottom: 13%;
  }

  .text-details {
      margin-left: 20rem;
      display: inline-block;
  }

  .welcome-text {
      position: absolute;
      width: 100%;
      margin-block-end: 0%;
      font-size: 300%;
      margin-top: -6.5rem;
      color: #023436
  }

  .profile-img {
      position: absolute;
      display: inline-block;
      width: 28%;
  }

  .manage-text {
      margin-top: 10%;
      margin-bottom: -20%;
      margin-left: -10rem;
      width: 80%;
  }

  .manage {
      margin-left: -5rem;
      margin-top: -1.2%;
      color: #023436;
      position: absolute;
      font-size: 1.5rem;
  }

  .under-details {

  }

  .notification-text {

      margin-top: 22%;
      margin-left: 70%;
      width: 100%;
      color: #023436;
      font-weight: 500;
  }

  .my-plants {

    margin-top: 5%;
    margin-left: 70%;
    width: 60%;
    color: #023436;
    font-weight: 500;
    text-decoration: underline;

  }

  .plant-link {
    color: #023436;

  }

  .sidebar-details {

  }

.side-bar {
  margin-left: 5%;
  display: inline-block;
}

.sidebar-item {
  display: block;
  margin-top: 1%;
  padding: 0%;
  width: 100%;
  font-size: 1.3rem;
  background-color: transparent;
}

.item-divider {
  margin-top: 6%;
  width: 100%;
  border-top: 1px solid black;
}

.tab {
  display: inline;
  tab-size: 2px;
}

.active-item {
  font-weight: 700;
}

.inactive:hover {
  font-weight: 600;
}

.user-details {
  display: inline-block;
  margin-top: 3%;
  margin-left: 10%;
  margin-right: -50%;
  position: absolute;
}

.user-card {
  background-color: #CDEAD1;
  width: 220%;
  padding-top: 20%;
  padding-bottom: 30%;
  padding-right: 10%;
  border-radius: 10%;
}

.detail-item {
  margin-left: 10%;
  margin-top: 6%;
  font-size: 1.5rem;
  margin-bottom: 1%;
  color: #023436;
}
</style>
