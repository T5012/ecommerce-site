<template>
  <h1>Shopping Cart</h1>
  <div v-if="cartItems.length > 0">
      <button class="remove-button"> Remove from cart</button>
    </div>
  <div v-if="cartItems.length === 0"> Please add items to cart!</div>
  <button class="checkout-button">Proceed to checkout</button>
  <ShoppingCartList :cartItems="cartItems" />
</template>
<script>
import { cartItems } from "@/temp-data";
import ShoppingCartList from "@/components/ShoppingCartList.vue";

export default {
  name: "ShoppingCartPage",
  data() {
    return {
      cartItems,
    };
  },
  components: {
    ShoppingCartList,
  },
};
</script>