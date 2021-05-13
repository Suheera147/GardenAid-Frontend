<template>
  <div class="page">
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

    <div class="image-text">
      <div class="text-details">
        <h2 class="welcome-text">HELLO, JOHN DOE !</h2>

        <div class="under-details">
          <div class="manage-text">
            <h2 class="manage">MANAGE MY ACCOUNT</h2>
          </div>

          <div class="flex">
            <div class="sidebar-details">
              <div class="side-bar">
                <button
                  type="button"
                  class="btn sidebar-item text-left inactive"
                  v-on:click="goToProfile()"
                >
                  My Profile
                  <pre class="tab">&nbsp;&nbsp;&nbsp;&nbsp;&emsp;</pre>
                  <i class="fas fa-arrow-circle-right"></i>
                  <hr class="item-divider text-left" />
                </button>
                <button
                  type="button"
                  class="btn sidebar-item text-left active-item"
                >
                  My Plants
                  <pre class="tab">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</pre>
                  <i class="fas fa-arrow-circle-right"></i>
                  <hr class="item-divider text-left" />
                </button>
                <button
                  type="button"
                  class="btn sidebar-item text-left inactive"
                >
                  My Address
                  <pre class="tab">&nbsp;&nbsp;&nbsp;&nbsp;</pre>
                  <i class="fas fa-arrow-circle-right"></i>
                  <hr class="item-divider text-left" />
                </button>
                <button
                  type="button"
                  class="btn sidebar-item text-left inactive"
                  v-on:click="goToOrders()"
                >
                  My Orders
                  <pre class="tab">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</pre>
                  <i class="fas fa-arrow-circle-right text-right"></i>
                  <hr class="item-divider text-left" />
                </button>
                <button
                  type="button"
                  class="btn sidebar-item text-left inactive"
                >
                  My Reviews
                  <pre class="tab">&nbsp;&nbsp;&nbsp;&nbsp;</pre>
                  <i class="fas fa-arrow-circle-right"></i>
                  <hr class="item-divider text-left" />
                </button>
                <button
                  type="button"
                  class="btn sidebar-item text-left inactive"
                >
                  My Favourites
                  <pre class="tab">&nbsp;&nbsp;</pre>
                  <i class="fas fa-arrow-circle-right"></i>
                  <hr class="item-divider text-left" />
                </button>
              </div>
            </div>
            <div class="notifications">
              <div class="notification-text">
                <svg
                  width="30"
                  height="30"
                  viewBox="0 0 22 22"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M9.9 7.7H12.1V5.5H9.9V7.7ZM11 19.8C6.149 19.8 2.2 15.851 2.2 11C2.2 6.149 6.149 2.2 11 2.2C15.851 2.2 19.8 6.149 19.8 11C19.8 15.851 15.851 19.8 11 19.8ZM11 0C9.55546 0 8.12506 0.284523 6.79048 0.837325C5.4559 1.39013 4.24327 2.20038 3.22183 3.22183C1.15893 5.28473 0 8.08262 0 11C0 13.9174 1.15893 16.7153 3.22183 18.7782C4.24327 19.7996 5.4559 20.6099 6.79048 21.1627C8.12506 21.7155 9.55546 22 11 22C13.9174 22 16.7153 20.8411 18.7782 18.7782C20.8411 16.7153 22 13.9174 22 11C22 9.55546 21.7155 8.12506 21.1627 6.79048C20.6099 5.4559 19.7996 4.24327 18.7782 3.22183C17.7567 2.20038 16.5441 1.39013 15.2095 0.837325C13.8749 0.284523 12.4445 0 11 0ZM9.9 16.5H12.1V9.9H9.9V16.5Z"
                    fill="#023436"
                  />
                </svg>
                <p>1 plant(s) needs watering right now!</p>
              </div>
              <div class="plant_container" id="plant1">
                <img src="/img/plants/plant1.png" alt="" />
                <div>
                  <div class="plant_header">
                    <div>
                      <p>Mealy sage - Salvia farinacea</p>
                      <p>40% Humidity</p>
                    </div>
                    <div>
                      <p>45 weeks</p>
                      <p>150 ppm</p>
                    </div>
                  </div>
                  <div class="plant_info">
                    <div>
                      <svg
                        width="20"
                        height="20"
                        viewBox="0 0 23 22"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M15.3275 11.3223C14.9836 11.3285 14.6443 11.4025 14.329 11.5401C14.0137 11.6778 13.7285 11.8763 13.4897 12.1244C13.2509 12.3725 13.0633 12.6653 12.9374 12.9861C12.8116 13.3069 12.75 13.6494 12.7562 13.9941C12.7624 14.3387 12.8363 14.6788 12.9736 14.9949C13.1109 15.3109 13.309 15.5968 13.5566 15.8361C13.8041 16.0754 14.0963 16.2636 14.4164 16.3897C14.7365 16.5159 15.0782 16.5776 15.4221 16.5715C16.1166 16.5589 16.7777 16.2704 17.2599 15.7694C17.7421 15.2683 18.006 14.5958 17.9934 13.8997C17.9872 13.555 17.9133 13.215 17.776 12.8989C17.6387 12.5828 17.4406 12.297 17.193 12.0577C16.6931 11.5743 16.022 11.3098 15.3275 11.3223ZM15.5072 21.2957C11.4641 21.3685 8.11586 18.1418 8.04266 14.079C7.94335 8.56738 15.1289 0.299093 15.1289 0.299093C15.1289 0.299093 22.6076 8.30316 22.7069 13.8148C22.7421 15.7638 22.0032 17.6469 20.653 19.0499C19.3028 20.4528 17.4518 21.2606 15.5072 21.2957ZM8.93878 5.66148L5.79643 5.7181L5.85318 8.86759L3.75828 8.90533L3.70153 5.75584L0.559187 5.81246L0.521355 3.7128L3.6637 3.65619L3.60696 0.506696L5.70185 0.46895L5.7586 3.61844L8.90095 3.56182L8.93878 5.66148Z"
                          fill="#446FA3"
                        />
                      </svg>
                      <span>300ml right now!</span>
                    </div>
                  </div>
                </div>
                <div v-on:click="dsd()" class="plant_details">
                  More Details >
                </div>
              </div>

              <div class="plant_container" id="plant2">
                <img src="/img/plants/plant1.png" alt="" />
                <div>
                  <div class="plant_header">
                    <div>
                      <p>African evergreen</p>
                      <p>70% Humidity</p>
                    </div>
                    <div>
                      <p>55 weeks</p>
                      <p>100 ppm</p>
                    </div>
                  </div>
                  <div class="plant_info">
                    <div>
                      <svg
                        width="20"
                        height="20"
                        viewBox="0 0 23 22"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M15.3275 11.3223C14.9836 11.3285 14.6443 11.4025 14.329 11.5401C14.0137 11.6778 13.7285 11.8763 13.4897 12.1244C13.2509 12.3725 13.0633 12.6653 12.9374 12.9861C12.8116 13.3069 12.75 13.6494 12.7562 13.9941C12.7624 14.3387 12.8363 14.6788 12.9736 14.9949C13.1109 15.3109 13.309 15.5968 13.5566 15.8361C13.8041 16.0754 14.0963 16.2636 14.4164 16.3897C14.7365 16.5159 15.0782 16.5776 15.4221 16.5715C16.1166 16.5589 16.7777 16.2704 17.2599 15.7694C17.7421 15.2683 18.006 14.5958 17.9934 13.8997C17.9872 13.555 17.9133 13.215 17.776 12.8989C17.6387 12.5828 17.4406 12.297 17.193 12.0577C16.6931 11.5743 16.022 11.3098 15.3275 11.3223ZM15.5072 21.2957C11.4641 21.3685 8.11586 18.1418 8.04266 14.079C7.94335 8.56738 15.1289 0.299093 15.1289 0.299093C15.1289 0.299093 22.6076 8.30316 22.7069 13.8148C22.7421 15.7638 22.0032 17.6469 20.653 19.0499C19.3028 20.4528 17.4518 21.2606 15.5072 21.2957ZM8.93878 5.66148L5.79643 5.7181L5.85318 8.86759L3.75828 8.90533L3.70153 5.75584L0.559187 5.81246L0.521355 3.7128L3.6637 3.65619L3.60696 0.506696L5.70185 0.46895L5.7586 3.61844L8.90095 3.56182L8.93878 5.66148Z"
                          fill="#446FA3"
                        />
                      </svg>
                      <span>500ml in 2 days</span>
                    </div>
                  </div>
                </div>
                <div class="plant_details">More Details ></div>
              </div>

              <div class="plant_container" id="plant3">
                <img src="/img/plants/plant1.png" alt="" />
                <div>
                  <div class="plant_header">
                    <div>
                      <p>African bowstring-hemp</p>
                      <p>65% Humidity</p>
                    </div>
                    <div>
                      <p>60 weeks</p>
                      <p>120 ppm</p>
                    </div>
                  </div>
                  <div class="plant_info">
                    <div>
                      <svg
                        width="20"
                        height="20"
                        viewBox="0 0 23 22"
                        fill="none"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M15.3275 11.3223C14.9836 11.3285 14.6443 11.4025 14.329 11.5401C14.0137 11.6778 13.7285 11.8763 13.4897 12.1244C13.2509 12.3725 13.0633 12.6653 12.9374 12.9861C12.8116 13.3069 12.75 13.6494 12.7562 13.9941C12.7624 14.3387 12.8363 14.6788 12.9736 14.9949C13.1109 15.3109 13.309 15.5968 13.5566 15.8361C13.8041 16.0754 14.0963 16.2636 14.4164 16.3897C14.7365 16.5159 15.0782 16.5776 15.4221 16.5715C16.1166 16.5589 16.7777 16.2704 17.2599 15.7694C17.7421 15.2683 18.006 14.5958 17.9934 13.8997C17.9872 13.555 17.9133 13.215 17.776 12.8989C17.6387 12.5828 17.4406 12.297 17.193 12.0577C16.6931 11.5743 16.022 11.3098 15.3275 11.3223ZM15.5072 21.2957C11.4641 21.3685 8.11586 18.1418 8.04266 14.079C7.94335 8.56738 15.1289 0.299093 15.1289 0.299093C15.1289 0.299093 22.6076 8.30316 22.7069 13.8148C22.7421 15.7638 22.0032 17.6469 20.653 19.0499C19.3028 20.4528 17.4518 21.2606 15.5072 21.2957ZM8.93878 5.66148L5.79643 5.7181L5.85318 8.86759L3.75828 8.90533L3.70153 5.75584L0.559187 5.81246L0.521355 3.7128L3.6637 3.65619L3.60696 0.506696L5.70185 0.46895L5.7586 3.61844L8.90095 3.56182L8.93878 5.66148Z"
                          fill="#446FA3"
                        />
                      </svg>
                      <span>400ml in 50 mins</span>
                    </div>
                  </div>
                </div>
                <div class="plant_details">More Details ></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Profile",

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
.navbar-background {
  background-color: rgba(107, 170, 117, 0.2);
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

.active {
  border-radius: 2rem;
  margin-left: 2rem !important;
  text-decoration: underline;
  font-weight: 650;
}

.image-text {
  display: inline-block;
  width: 100%;
  padding: 5% 0;
  background-color: rgba(107, 170, 117, 0.2);
}

.profile-image {
  margin-left: 20%;
  display: inline-block;
  width: 10%;
  padding-bottom: 13%;
}

.text-details {
  display: inline-block;
  margin-left: 56px;
}

.welcome-text {
  width: 100%;
  margin-block-end: 0%;
  font-size: 300%;
  color: #023436;
  letter-spacing: 2px;
}

.active-item i {
  margin-left: -10px;
}

.profile-img {
  position: absolute;
  display: inline-block;
  width: 28%;
}

.manage-text {
  margin-top: 10%;
}

.manage {
  color: #023436;
  font-size: 1.5rem;
}

.under-details {
}

.notification-text {
  width: 100%;
  color: #023436;
  font-weight: 500;
  font-size: 24px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.notification-text p {
  margin: 0;
  margin-left: 10px;
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
  margin-top: 133px;
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
  width: 500%;
  padding-top: 20%;
  padding-bottom: 120%;
  padding-right: 100%;
  border-radius: 10%;
}

.detail-item {
  margin-left: 10%;
  margin-top: 6%;
  font-size: 1.5rem;
  margin-bottom: 1%;
  color: #023436;
}

#plant1 {
  background-color: #b3cdaf;
}
#plant2 {
  background-color: #bcddc1;
}
#plant3 {
  background-color: #87a486;
}

.plant_container {
  display: flex;
  margin-left: 100px;
  border-radius: 80px;
  padding: 12px 20px 23px 20px;
  margin-top: 35px;
  position: relative;
  width: 941px;
}

.plant_container img {
  width: 160px;
  height: 165px;
  margin-right: 34px;
}

.plant_header {
  display: flex;
  justify-content: space-between;
  margin-top: 33px;
}

.plant_header div:first-child {
  margin-right: 21px;
}

.plant_header p {
  font-size: 24px;
  font-weight: 500;
  margin: 0;
}

.plant_info div:first-of-type {
  margin-top: 7px;
  padding: 15px 190px 14px 20px;
  width: max-content;
  background-color: #a1c7be;
  display: flex;
  align-items: center;
  border-radius: 20px;
  box-shadow: 3px 3px 5px 0px rgba(0, 0, 0, 0.5);
}

.plant_info div:first-of-type span {
  font-size: 24px;
  font-weight: bold;
}

.plant_info svg {
  margin-right: 9px;
}

.plant_details {
  position: absolute;
  bottom: 20px;
  right: 67px;
  font-size: 18px;
  color: #656060;
  cursor: pointer;
  font-style: italic;
}

.plant_details:hover {
  text-decoration: underline;
}

.flex {
  display: flex;
}
</style>
