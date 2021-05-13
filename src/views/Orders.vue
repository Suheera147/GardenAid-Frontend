<template>
  <div style="background-color: rgba(107, 170, 117, 0.2)">
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
            <button class="btn btn-primary">My Cart</button>
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
        <h2 class="welcome-text">Hello John Doe!</h2>

        <div class="under-details">
          <div class="manage-text">
            <h2 class="manage">MANAGE MY ACCOUNT</h2>
          </div>
        </div>
      </div>
    </div>

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
          class="btn sidebar-item text-left inactive"
          v-on:click="goToPlants()"
        >
          My Plants
          <pre class="tab">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</pre>
          <i class="fas fa-arrow-circle-right"></i>
          <hr class="item-divider text-left" />
        </button>
        <button type="button" class="btn sidebar-item text-left inactive">
          My Address
          <pre class="tab">&nbsp;&nbsp;&nbsp;&nbsp;</pre>
          <i class="fas fa-arrow-circle-right"></i>
          <hr class="item-divider text-left" />
        </button>
        <button type="button" class="btn sidebar-item text-left active-item">
          My Orders
          <pre class="tab">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</pre>
          <i class="fas fa-arrow-circle-right text-right"></i>
          <hr class="item-divider text-left" />
        </button>
        <button type="button" class="btn sidebar-item text-left inactive">
          My Reviews
          <pre class="tab">&nbsp;&nbsp;&nbsp;&nbsp;</pre>
          <i class="fas fa-arrow-circle-right"></i>
          <hr class="item-divider text-left" />
        </button>
        <button type="button" class="btn sidebar-item text-left inactive">
          My Favourites
          <pre class="tab">&nbsp;&nbsp;</pre>
          <i class="fas fa-arrow-circle-right"></i>
          <hr class="item-divider text-left" />
        </button>
      </div>

      <div class="orders-info">
        <div class="orders-header">
          <div class="orders-text">My Orders</div>

          <div class="header-search">
            <form class="form-inline my-2 my-lg-0">
              <input
                class="form-control ml-sm-2 search-bar"
                type="search"
                placeholder="Search"
                aria-label="Search"
              />
            </form>
          </div>

          <div class="dropdown-div">
            <button>DropDown</button>
          </div>
        </div>
        <div class="order">
          <div class="card">
            <div class="card-header">
              <div class="card-date">
                <div class="date-header">Order Date</div>
                <div class="date-value">10-05-15</div>
              </div>
              <div class="card-receiver">
                <div class="receiver-header">Reciever</div>
                <div class="receiver-value">John Doe</div>
              </div>
              <div class="card-amount">
                <div class="amount-header">Amount</div>
                <div class="amount-value">X.XX TL</div>
              </div>
              <div class="details-btn">
                <button class="btn btn-success">Order Details</button>
              </div>
            </div>
            <div class="card-body">
              <div class="order-img">
                <img
                  alt="garden-aid logo"
                  class="order-image"
                  src="../assets/dummy.png"
                />
              </div>
              <div class="order-name-status">
                <div class="order-name">Product Name</div>
                <div class="order-status">
                  <i class="far fa-thumbs-up"></i>
                  Delivered
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="order"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Profile",

  methods: {
    goToOrders() {
      this.$router.push("/profile/orders");
    },

    logout() {
      localStorage.removeItem("id");
      localStorage.removeItem("number");
      localStorage.removeItem("name");
      localStorage.removeItem("email");
      this.$router.push("/login");
    },
    goToPlants() {
      this.$router.push("/profile/plants");
    },

    goToProfile() {
      this.$router.push("/profile");
    },
  },
};
</script>

<style scoped>
.logo-img {
  width: 80%;
  height: 80%;
}

.nav-items-div {
  margin-top: 2rem;
  margin-right: 6rem;
}

.search-bar {
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

.btn-primary {
  margin-left: 2rem;
  background-color: #023436;
  border: none;
  width: 7rem;
}

.btn-danger {
  margin-left: 2rem;
  background-color: #5b3b19;
  border: none;
  width: 7rem;
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

.notification-text {
  margin-top: 22%;
  margin-left: 70%;
  width: 70%;
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
  margin-top: 5%;
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
  font-weight: 700 !important;
}

.inactive:hover {
  font-weight: 600;
}

.orders-info {
  margin-left: 10%;
  position: absolute;
  display: inline-block;
}

.orders-header {
  border: solid;
  border-width: 0.15rem;
  margin-top: -5%;
  width: 150%;
  padding-left: 3%;
  padding-bottom: 1%;
}

.header-search {
  margin-left: 10%;
  display: inline-block !important;
  margin-top: 0% !important;
}

.orders-text {
  display: inline-block;
  padding-top: 1%;
  padding-bottom: 1%;
  font-size: 1.5rem;
  color: #023436;
  font-weight: 500;
  font-style: italic;
}

.dropdown-div {
  display: inline-block;
  margin-left: 15%;
}

.order {
  margin-top: 6%;
  width: 150%;
}

.card-header {
  padding-left: 5%;
  background-color: rgba(107, 170, 117, 0.15);
  border: 1px solid black;
}

.card-date {
  display: inline-block;
}

.date-header {
  font-weight: 700;
  font-size: 1.3rem;
  color: #023436;
}

.date-value {
  color: #023436;
  font-weight: 500;
}

.card-receiver {
  margin-left: 20%;
  display: inline-block;
}

.receiver-header {
  font-weight: 700;
  font-size: 1.3rem;
  color: #023436;
}

.receiver-value {
  color: #023436;
  font-weight: 500;
}

.amount-header {
  font-weight: 700;
  font-size: 1.3rem;
  color: #023436;
}

.amount-value {
  color: #023436;
  font-weight: 500;
}

.card-body {
  background-color: rgba(107, 170, 117, 0.2);
  border-bottom: 1px solid black;
  border-left: 1px solid black;
  border-right: 1px solid black;
}

.card-amount {
  margin-left: 20%;
  display: inline-block;
}

.details-btn {
  position: absolute;
  display: inline-block;
  margin-left: 10%;
  padding-top: 0.5rem;
}

.btn-success {
  width: 120%;
  border-radius: 0.4rem;
}

.order-img {
  display: inline-block;
}

.order-image {
  width: 13rem;
}

.order-name-status {
  margin-left: 7%;
  display: inline-block;
  position: absolute;
}

.order-name {
  color: #023436;
  font-size: 1.3rem;
  font-weight: 700;
}

.order-status {
  margin-top: 1rem;
  color: #a09e9e;
  font-weight: 500;
}

.fa-thumbs-up {
  color: #6baa75;
}
</style>
