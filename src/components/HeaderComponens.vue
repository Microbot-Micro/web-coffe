<template>
  <div>
    <!-- header section starts  -->
    <header class="header">
      <a href="#" class="logo">
        <img src="../assets/images/logo.png" alt="">
      </a>
      <nav class="navbar" :class="{ 'active': isNavbarActive }">
        <a href="#home">home</a>
        <a href="#about">about</a>
        <a href="#menu">menu</a>
        <a href="#products">products</a>
        <a href="#review">review</a>
        <a href="#contact">contact</a>
        <a href="#blogs">blogs</a>
      </nav>
      <div class="icons">
        <div class="fas fa-search" id="search-btn" @click="toggleSearch"></div>
        <div class="fas fa-shopping-cart" id="cart-btn"></div>
        <div class="fas fa-bars" id="menu-btn" @click="toggleNavbar"></div>
      </div>
      <div class="search-form" v-show="isSearchVisible">
        <input type="search" id="search-box" placeholder="search here...">
        <label for="search-box" class="fas fa-search"></label>
      </div>

      <div class="cart-items-container">
        <div class="cart-item">
          <span class="fas fa-times"></span>
          <img src="../assets/images/cart-item-1.png" alt="">
          <div class="content">
            <h3>cart item 01</h3>
            <div class="price">$15.99/-</div>
          </div>
        </div>
        <div class="cart-item">
          <span class="fas fa-times"></span>
          <img src="../assets/images/cart-item-2.png" alt="">
          <div class="content">
            <h3>cart item 02</h3>
            <div class="price">$15.99/-</div>
          </div>
        </div>
        <div class="cart-item">
          <span class="fas fa-times"></span>
          <img src="../assets/images/cart-item-3.png" alt="">
          <div class="content">
            <h3>cart item 03</h3>
            <div class="price">$15.99/-</div>
          </div>
        </div>
        <div class="cart-item">
          <span class="fas fa-times"></span>
          <img src="../assets/images/cart-item-4.png" alt="">
          <div class="content">
            <h3>cart item 04</h3>
            <div class="price">$15.99/-</div>
          </div>
        </div>
        <a href="#" class="btn">checkout now</a>
      </div>

    </header>
    <!-- header section ends -->
  </div>
</template>

<script>
export default {
  name: "HeaderComponents",
  data() {
    return {
      isSearchVisible: false,
      isNavbarActive: false,
    };
  },
  methods: {
    toggleNavbar() {
      this.isNavbarActive = !this.isNavbarActive;
      if (!this.isNavbarActive) {
        window.addEventListener('scroll', this.closeNavbarOnScroll);
      } else {
        window.removeEventListener('scroll', this.closeNavbarOnScroll);
      }
    },
    toggleSearch() {
      this.isSearchVisible = !this.isSearchVisible;
    },
    closeNavbarOnScroll() {
      this.isNavbarActive = false;
      window.removeEventListener('scroll', this.closeNavbarOnScroll);
    },
  },
};
</script>

<style lang="scss" scoped>
/* Tambahkan gaya untuk navbar yang aktif */
.active {
  display: block !important; /* !important digunakan untuk memastikan gaya ini diaplikasikan */
  text-align: center;

}
</style>
