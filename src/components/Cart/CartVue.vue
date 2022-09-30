<template>
  <CartProductlist :cart="cart"></CartProductlist>
</template>
  
<script>

import CartProductlist from './CartProductList.vue';
import { eventBus } from '../../main';

export default {
  components: {
    CartProductlist,
  },
  data() {
   return {
      cart : []
   }
  },
  created(){
    this.cart = eventBus.cart;
    eventBus.$on('update:cart', (cart) => {
      this.cart = cart;
    });
  }
}
</script>
  
<style>

</style>