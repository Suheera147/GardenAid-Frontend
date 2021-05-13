<template>
  <div class="home">
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
            <a class="nav-link active" href="/home">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">About</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Contact</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="/profile">My Profile</a>
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

    <div class="home-text">
      <h1 class="text-center">Welcome to GardenAid!</h1>
    </div>

    <hr class="ruler bg" />

    <div class="featured-div">
      <h2 class="text-center">Featured Products</h2>

      <div class="swiper-container">
        <swiper class="swiper" :options="swiperOption">
          <swiper-slide>
            <div class="card">
              <div class="card-body text-center">
                <img
                  alt="garden-aid logo"
                  class="slide-img"
                  src="../assets/dummy.png"
                />

                <div class="slide-name">Hayacinth</div>
                <div class="slide-price">100TL</div>
                <div class="slide-rating">
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star-half-alt"></i>
                  <i class="far fa-star"></i>
                </div>
              </div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="card">
              <div class="card-body text-center">
                <img
                  alt="garden-aid logo"
                  class="slide-img"
                  src="../assets/dummy.png"
                />

                <div class="slide-name">Hayacinth</div>
                <div class="slide-price">100TL</div>
                <div class="slide-rating">
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star-half-alt"></i>
                  <i class="far fa-star"></i>
                </div>
              </div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="card">
              <div class="card-body text-center">
                <img
                  alt="garden-aid logo"
                  class="slide-img"
                  src="../assets/dummy.png"
                />

                <div class="slide-name">Hayacinth</div>
                <div class="slide-price">100TL</div>
                <div class="slide-rating">
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star-half-alt"></i>
                  <i class="far fa-star"></i>
                </div>
              </div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="card">
              <div class="card-body text-center">
                <img
                  alt="garden-aid logo"
                  class="slide-img"
                  src="../assets/dummy.png"
                />

                <div class="slide-name">Hayacinth</div>
                <div class="slide-price">100TL</div>
                <div class="slide-rating">
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star-half-alt"></i>
                  <i class="far fa-star"></i>
                </div>
              </div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="card">
              <div class="card-body text-center">
                <img
                  alt="garden-aid logo"
                  class="slide-img"
                  src="../assets/dummy.png"
                />

                <div class="slide-name">Hayacinth</div>
                <div class="slide-price">100TL</div>
                <div class="slide-rating">
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star-half-alt"></i>
                  <i class="far fa-star"></i>
                </div>
              </div>
            </div>
          </swiper-slide>
          <swiper-slide>
            <div class="card">
              <div class="card-body text-center">
                <img
                  alt="garden-aid logo"
                  class="slide-img"
                  src="../assets/dummy.png"
                />

                <div class="slide-name">Hayacinth</div>
                <div class="slide-price">100TL</div>
                <div class="slide-rating">
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star"></i>
                  <i class="fas fa-star-half-alt"></i>
                  <i class="far fa-star"></i>
                </div>
              </div>
            </div>
          </swiper-slide>
          <div class="swiper-pagination" slot="pagination"></div>
          <div class="swiper-button-prev" slot="button-prev"></div>
          <div class="swiper-button-next" slot="button-next"></div>
        </swiper>
      </div>
    </div>

    <hr class="ruler bg" />

    <div class="products-div">
      <h2 class="h-product col-left">All Products</h2>

      <div class="dropdown sort-btn">
        <button>Dropdown</button>
      </div>

      <div class="product">
        <div class="product-image" v-on:click="goToProduct()">
          <img
            alt="garden-aid logo"
            class="slide-img"
            src="../assets/dummy.png"
          />
        </div>
        <div class="product-detail">
          <div class="prod-name-rate">
            <div class="prod-name">Hayacinth</div>
            <div class="prod-rate">
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star-half-alt"></i>
              <i class="far fa-star"></i>
            </div>
          </div>
          <div class="prod-price">100 TL</div>
          <div class="prod-desc">
            Product Description : Lorem Ipsum Lorem Ipsum Lorem Ipsum Lorem
            Ipsum Lorem Ipsum Lorem Ipsum Lorem Ipsum Lorem Ipsum Lorem Ipsum
          </div>
          <div class="prod-ship">Ships to Turkey!</div>
        </div>
      </div>

      <hr class="ruler" />

      <div class="product">
        <div class="product-image" v-on:click="goToProduct()">
          <img
            alt="garden-aid logo"
            class="slide-img"
            src="../assets/dummy.png"
          />
        </div>
        <div class="product-detail">
          <div class="prod-name-rate">
            <div class="prod-name">Hayacinth</div>
            <div class="prod-rate">
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star"></i>
              <i class="fas fa-star-half-alt"></i>
              <i class="far fa-star"></i>
            </div>
          </div>
          <div class="prod-price">100 TL</div>
          <div class="prod-desc">
            Product Description : Lorem Ipsum Lorem Ipsum Lorem Ipsum Lorem
            Ipsum Lorem Ipsum Lorem Ipsum Lorem Ipsum Lorem Ipsum Lorem Ipsum
          </div>
          <div class="prod-ship">Ships to Turkey!</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import { Swiper, SwiperSlide } from "vue-awesome-swiper";
import "swiper/css/swiper.css";

export default {
  name: "Home",

  components: {
    Swiper,
    SwiperSlide,
  },

  methods: {
    goToProduct() {
      this.$router.push("/product/1");
    },
  },

  data() {
    return {
      swiperOption: {
        slidesPerView: 3,
        spaceBetween: 20,
        pagination: {
          el: ".swiper-pagination",
          clickable: true,
        },
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev",
        },
      },
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
.card {
  border: 0;
}

.card-body {
  background-color: rgba(107, 170, 117, 0.2);
}

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

.active {
  border-radius: 2rem;
  margin-left: 2rem !important;
  text-decoration: underline;
  font-weight: 650;
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

.home-text {
  padding-top: 3rem;
  padding-bottom: 3rem;
  background-color: rgba(107, 170, 117, 0.2);
}

.ruler {
  border-top: 4px solid #c5bcbc;
  padding-bottom: 3rem;
  margin: 0;
}

.ruler.bg {
  background-color: rgba(107, 170, 117, 0.2);
}

.featured-div {
  background-color: rgba(107, 170, 117, 0.2);
}

.swiper-container {
  margin-top: 2rem;
  margin-left: 6%;
  width: 88%;
  margin-right: 6%;
  padding-left: 1rem;
  padding-bottom: 4rem;
}

.swiper-button-prev {
  margin-left: -0.5rem;
}

.slide-img {
  width: 100%;
}

.slide-name {
  margin-top: 1rem;
  color: #023436 !important;
  font-weight: 600;
}

.slide-price {
  color: #023436 !important;
  font-weight: 600;
}

.h-product {
  padding-left: 7rem;
  display: inline-block;
  color: #145d60;
}

.sort-btn {
  display: inline-block;
  padding-left: 60%;
  padding-bottom: 5%;
}

.product {
  padding-left: 4rem;
  width: 100%;
  padding-bottom: 3rem;
}

.products-div {
  background-color: rgba(107, 170, 117, 0.2);
}

.product-image {
  display: inline-block;
  width: 25%;
  cursor: pointer;
}

.product-detail {
  display: inline-block;
  margin-left: 4rem;
  width: 60%;
}

.prod-name-rate {
  display: block;
}

.prod-name {
  display: inline-block;
  color: #023436;
  font-weight: 600;
}

.prod-rate {
  margin-left: 2rem;
  display: inline-block;
  color: #023436;
  font-weight: 600;
}

.prod-price {
  display: block;
  color: #023436;
  margin-top: 1rem;
  font-weight: 600;
}

.prod-desc {
  display: block;
  color: #5e5e5e;
  font-weight: 600;
  max-height: 15rem;
  max-width: 35rem;
  overflow-wrap: break-word;
  margin-bottom: -2rem;
}

.prod-ship {
  position: absolute;
  margin-top: 4rem;
}
</style>
