<template>
  <div id="app">
    <the-header></the-header>
    <div class="d-flex flex-row">
      <shop-vue class="w-75"></shop-vue>
      <cart-vue class="w-25"></cart-vue>
    </div>
  </div>
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import ShopVue from './components/Shop/ShopVue.vue';
import CartVue from './components/Cart/CartVue.vue';



export default {
  name: 'app',
  components: {
    TheHeader,
    ShopVue,
    CartVue,
}
}
</script>

<style>

</style>