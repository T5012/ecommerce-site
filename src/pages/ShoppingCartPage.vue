<template>
  <h1>Shopping Cart</h1>
  <div v-if="cartItems.length > 0">
    <div class="product-container" v-for="item in cartItems" :key="item.id">
      <img class="product-image" :src="item.imageName"/>
      <div class="details-wrap">
        <h3>{{item.name}}</h3>
        <p>{{item.price}}</p>
      </div>
      <button class="remove-button"> Remove from cart</button>
    </div>
  </div>
  <div v-if="cartItems.length === 0"> Please add items to cart!</div>
  <button class="checkout-button">Proceed to checkout</button>
</template>
<script>
import {cartItems} from "@/temp-data";

export default {
  name: "ShoppingCartPage",
  data(){
    return {
      cartItems,
    }
  }
}
</script>