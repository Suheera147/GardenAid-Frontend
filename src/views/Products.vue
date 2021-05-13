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
            <a class="nav-link active" href="/profile">My Profile</a>
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

    <div class="main">
      <div class="productInfo">
        <div class="productInfo__left">
          <img src="/img/plantProduct.png" alt="" />
        </div>
        <div class="productInfo__right">
          <h2>Common Hyacinth - Muscari</h2>
          <div class="productInfo__reviews">
            <div>
              <svg
                width="18"
                height="17"
                viewBox="0 0 18 17"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M9 13.5L3.70993 16.2812L4.72025 10.3906L0.440491 6.21885L6.35497 5.35942L9 0L11.645 5.35942L17.5595 6.21885L13.2798 10.3906L14.2901 16.2812L9 13.5Z"
                  fill="#023436"
                />
              </svg>
              <svg
                width="18"
                height="17"
                viewBox="0 0 18 17"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M9 13.5L3.70993 16.2812L4.72025 10.3906L0.440491 6.21885L6.35497 5.35942L9 0L11.645 5.35942L17.5595 6.21885L13.2798 10.3906L14.2901 16.2812L9 13.5Z"
                  fill="#023436"
                />
              </svg>
              <svg
                width="18"
                height="17"
                viewBox="0 0 18 17"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M9 13.5L3.70993 16.2812L4.72025 10.3906L0.440491 6.21885L6.35497 5.35942L9 0L11.645 5.35942L17.5595 6.21885L13.2798 10.3906L14.2901 16.2812L9 13.5Z"
                  fill="#023436"
                />
              </svg>
              <svg
                width="18"
                height="17"
                viewBox="0 0 18 17"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M9 13.5L3.70993 16.2812L4.72025 10.3906L0.440491 6.21885L6.35497 5.35942L9 0L11.645 5.35942L17.5595 6.21885L13.2798 10.3906L14.2901 16.2812L9 13.5Z"
                  fill="#94989E"
                />
              </svg>
              <svg
                width="18"
                height="17"
                viewBox="0 0 18 17"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M9 13.5L3.70993 16.2812L4.72025 10.3906L0.440491 6.21885L6.35497 5.35942L9 0L11.645 5.35942L17.5595 6.21885L13.2798 10.3906L14.2901 16.2812L9 13.5Z"
                  fill="#94989E"
                />
              </svg>
            </div>
            <p>17 reviews</p>
            <div class="shareIcon">
              <svg
                width="20"
                height="22"
                viewBox="0 0 20 22"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M16.6667 15.5581C15.8222 15.5581 15.0667 15.8896 14.4889 16.409L6.56667 11.8233C6.62222 11.5692 6.66667 11.315 6.66667 11.0498C6.66667 10.7847 6.62222 10.5305 6.56667 10.2764L14.4 5.73493C15 6.28742 15.7889 6.62996 16.6667 6.62996C17.5507 6.62996 18.3986 6.28071 19.0237 5.65904C19.6488 5.03737 20 4.19421 20 3.31504C20 2.43587 19.6488 1.59271 19.0237 0.971039C18.3986 0.349371 17.5507 0.00012207 16.6667 0.00012207C15.7826 0.00012207 14.9348 0.349371 14.3096 0.971039C13.6845 1.59271 13.3333 2.43587 13.3333 3.31504C13.3333 3.58023 13.3778 3.83438 13.4333 4.08852L5.6 8.62996C5 8.07747 4.21111 7.73493 3.33333 7.73493C2.44928 7.73493 1.60143 8.08418 0.976311 8.70584C0.35119 9.32751 0 10.1707 0 11.0498C0 11.929 0.35119 12.7722 0.976311 13.3938C1.60143 14.0155 2.44928 14.3648 3.33333 14.3648C4.21111 14.3648 5 14.0222 5.6 13.4697L13.5111 18.0554C13.4556 18.2874 13.4222 18.5305 13.4222 18.7847C13.4222 20.5637 14.8778 22.0001 16.6667 22.0001C18.4556 22.0001 19.9111 20.5637 19.9111 18.7847C19.9111 17.9289 19.5693 17.1082 18.9608 16.5032C18.3524 15.8981 17.5271 15.5581 16.6667 15.5581Z"
                  fill="#264653"
                />
              </svg>
            </div>
          </div>
          <div class="productInfo__price">
            <p>100 TL</p>
            <select>
              <option value="0">No. of Pieces</option>
              <option value="1">1</option>
              <option value="2">2</option>
              <option value="3">3</option>
              <option value="4">4</option>
            </select>
          </div>
          <div class="productInfo__info">
            Muscari is a genus of perennial bulbous plants native to Eurasia
            that produce spikes of dense, most commonly blue, urn-shaped flowers
            resembling bunches of grapes in the spring.
          </div>
          <div class="productInfo__nav">
            <button class="productInfo__addToCart">Add to Cart</button>
            <button>Buy Now</button>
          </div>
        </div>
      </div>
      <div class="break"></div>
      <div class="reviews">
        <h1>Reviews</h1>
        <div class="review">
          <img src="/img/users/user1.png" alt="" />
          <div class="review__user">
            <p>Jane Doe</p>
            <p>12 August, 2018</p>
            <p>
              <svg
                width="18"
                height="17"
                viewBox="0 0 18 17"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M9 13.5L3.70993 16.2812L4.72025 10.3906L0.440491 6.21885L6.35497 5.35942L9 0L11.645 5.35942L17.5595 6.21885L13.2798 10.3906L14.2901 16.2812L9 13.5Z"
                  fill="#023436"
                />
              </svg>
              <svg
                width="18"
                height="17"
                viewBox="0 0 18 17"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M9 13.5L3.70993 16.2812L4.72025 10.3906L0.440491 6.21885L6.35497 5.35942L9 0L11.645 5.35942L17.5595 6.21885L13.2798 10.3906L14.2901 16.2812L9 13.5Z"
                  fill="#023436"
                />
              </svg>
              <svg
                width="18"
                height="17"
                viewBox="0 0 18 17"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M9 13.5L3.70993 16.2812L4.72025 10.3906L0.440491 6.21885L6.35497 5.35942L9 0L11.645 5.35942L17.5595 6.21885L13.2798 10.3906L14.2901 16.2812L9 13.5Z"
                  fill="#023436"
                />
              </svg>
              <svg
                width="18"
                height="17"
                viewBox="0 0 18 17"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M9 13.5L3.70993 16.2812L4.72025 10.3906L0.440491 6.21885L6.35497 5.35942L9 0L11.645 5.35942L17.5595 6.21885L13.2798 10.3906L14.2901 16.2812L9 13.5Z"
                  fill="#94989E"
                />
              </svg>
              <svg
                width="18"
                height="17"
                viewBox="0 0 18 17"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M9 13.5L3.70993 16.2812L4.72025 10.3906L0.440491 6.21885L6.35497 5.35942L9 0L11.645 5.35942L17.5595 6.21885L13.2798 10.3906L14.2901 16.2812L9 13.5Z"
                  fill="#94989E"
                />
              </svg>
            </p>
          </div>
          <div class="review__info">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam, quis nostrud exercitation ullamco laboris
          </div>
        </div>

        <div class="review">
          <img src="/img/users/user2.png" alt="" />
          <div class="review__user">
            <p>Jane Doe</p>
            <p>12 August, 2018</p>
            <p>
              <svg
                width="18"
                height="17"
                viewBox="0 0 18 17"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M9 13.5L3.70993 16.2812L4.72025 10.3906L0.440491 6.21885L6.35497 5.35942L9 0L11.645 5.35942L17.5595 6.21885L13.2798 10.3906L14.2901 16.2812L9 13.5Z"
                  fill="#023436"
                />
              </svg>
              <svg
                width="18"
                height="17"
                viewBox="0 0 18 17"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M9 13.5L3.70993 16.2812L4.72025 10.3906L0.440491 6.21885L6.35497 5.35942L9 0L11.645 5.35942L17.5595 6.21885L13.2798 10.3906L14.2901 16.2812L9 13.5Z"
                  fill="#023436"
                />
              </svg>
              <svg
                width="18"
                height="17"
                viewBox="0 0 18 17"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M9 13.5L3.70993 16.2812L4.72025 10.3906L0.440491 6.21885L6.35497 5.35942L9 0L11.645 5.35942L17.5595 6.21885L13.2798 10.3906L14.2901 16.2812L9 13.5Z"
                  fill="#023436"
                />
              </svg>
              <svg
                width="18"
                height="17"
                viewBox="0 0 18 17"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M9 13.5L3.70993 16.2812L4.72025 10.3906L0.440491 6.21885L6.35497 5.35942L9 0L11.645 5.35942L17.5595 6.21885L13.2798 10.3906L14.2901 16.2812L9 13.5Z"
                  fill="#94989E"
                />
              </svg>
              <svg
                width="18"
                height="17"
                viewBox="0 0 18 17"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  fill-rule="evenodd"
                  clip-rule="evenodd"
                  d="M9 13.5L3.70993 16.2812L4.72025 10.3906L0.440491 6.21885L6.35497 5.35942L9 0L11.645 5.35942L17.5595 6.21885L13.2798 10.3906L14.2901 16.2812L9 13.5Z"
                  fill="#94989E"
                />
              </svg>
            </p>
          </div>
          <div class="review__info">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam, quis nostrud exercitation ullamco laboris
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
      this.$router.push("/profile/orders");
    },
  },
};
</script>

<style scoped>
p {
  margin: 0;
}

.navbar-background {
  background-color: rgba(107, 170, 117, 0.2);
}

.main {
  background-color: rgba(107, 170, 117, 0.2);
  padding: 110px 172px 110px 25px;
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

.nav-link:hover {
  text-decoration: underline;
}

.active {
  border-radius: 2rem;
  margin-left: 2rem !important;
  text-decoration: underline;
  font-weight: 650;
}

.profile-image {
  margin-left: 20%;
  display: inline-block;
  width: 10%;
  padding-bottom: 13%;
}

.productInfo {
  display: flex;
  align-items: center;
  padding-bottom: 18px;
}

.break {
  height: 2px;
  border: 1px solid #c5bcbc;
  margin-left: -29px;
  width: 99vw;
}

.productInfo__right {
  margin-left: 50px;
}

.productInfo__reviews {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 60%;
  margin-bottom: 7px;
}

.productInfo__reviews p {
  margin: 0;
  font-size: 18px;
  color: #656060;
}

.shareIcon {
  margin-top: 8px;
}

.productInfo__price {
  display: flex;
  padding: 21px 0 12px 0;
  border-top: 1px solid #b2a1a1;
  border-bottom: 1px solid #b2a1a1;
  align-items: center;
}

.productInfo__price p {
  font-size: 24px;
  margin-right: 150px;
}

.productInfo__left {
  position: relative;
}

.productInfo__price select {
  width: 282px;
  border: 1px solid #ccc;
  padding: 5px 30px 5px 10px;
}

.productInfo__price select option {
  font-size: 18px;
}

.productInfo__info {
  width: 80%;
  margin-top: 18px;
  margin-bottom: 40px;
  font-size: 16px;
  color: #656060;
}

.productInfo__nav {
  display: flex;
}

.productInfo__nav button {
  width: 200px;
  font-size: 15px;
  border: none;
  outline: none;
  padding: 10px;
  color: white;
}

.productInfo__addToCart {
  background-color: #6baa75;
  margin-right: 56px;
}

.productInfo__nav button:last-child {
  background-color: #023436;
}

.reviews {
  margin: 13px 0 13px 45px;
  font-size: 36px;
  color: #656060;
}

.review {
  display: flex;
  margin-bottom: 17px;
}

.review__user {
  font-size: 18px;
  padding: 0 20px 17px 29px;
  border-bottom: 1px solid #c6b4b4;
}

.review img {
  padding-bottom: 30px;
  border-bottom: 1px solid #c6b4b4;
}

.review__info {
  font-size: 18px;
  width: 50%;
}
</style>
