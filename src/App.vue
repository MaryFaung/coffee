<template>
  <div id="app">
    <Preloader />
    <CoffeeHeader />
    <Banner />
    <div class="tm-main-section light-gray-bg">
      <div class="container" id="main">
        <CoffeeDesc />
        <CoffeeList />
        <CakeList />
        <CartList />
      </div>
    </div>
    <CoffeeFooter />
  </div>
</template>

<script>
import Preloader from "./components/Preloader.vue";
import CoffeeHeader from "./components/CoffeeHeader.vue";
import Banner from "./components/Banner.vue";
import CoffeeDesc from "./components/content/CoffeeDesc.vue";
import CoffeeList from "./components/content/CoffeeList.vue";
import CakeList from "./components/content/CakeList.vue";
import CartList from "./components/content/CartList.vue";
import CoffeeFooter from "./components/CoffeeFooter.vue";

export default {
  name: "app",
  components: {
    Preloader,
    CoffeeHeader,
    Banner,
    CoffeeDesc,
    CoffeeList,
    CakeList,
    CartList,
    CoffeeFooter
  }
};
</script>

<style>
</style>
