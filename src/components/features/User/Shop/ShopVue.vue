<template>
  <shop-product-list :products="products"></shop-product-list>
</template>
  
<script>

import ShopProductList from './ShopProductList.vue';
import { eventBus } from '../../../../main';

export default {
  components: {
    ShopProductList,
  },
  data() {
   return {
      products : []
   }
  },
  created(){
    this.products = eventBus.products;
    eventBus.$on('update:products', (products) => {
      this.products = products;
    });
  }
}
</script>
  
<style>

</style>