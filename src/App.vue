<template>
  <div>
    <HeaderComponens/>
    <HomeView/>
    <AboutView/>
    <MenuComponens/>
    <ProductComponens/>
    <CustomerComponens/>
    <ContactView/>
    <BlogComponens/>
    <FooterComponens/>
  </div>
</template>

<script>
import HeaderComponens from './components/HeaderComponens.vue';
import MenuComponens from './components/MenuComponens.vue';
import ProductComponens from './components/ProductComponens.vue';
import CustomerComponens from './components/CustomerComponens.vue';
import BlogComponens from './components/BlogComponens.vue';
import FooterComponens from './components/FooterComponens.vue';
import HomeView from './views/HomeView.vue';
import AboutView from './views/AboutView.vue';
import ContactView from './views/ContactView.vue';
  export default {
    name: "App",
    components: {
      HeaderComponens,
      HomeView,
      AboutView,
      MenuComponens,
      ProductComponens,
      CustomerComponens,
      ContactView,
      BlogComponens,
      FooterComponens,
    }
  }
</script>

<style lang="scss" scoped>

</style>