<template>
  <div class="product-container" v-for="item in cartItems" :key="item.id">
    <img class="product-image" :src="item.imageName"/>
    <div class="details-wrap">
      <h3>{{item.name}}</h3>
      <p>{{item.price}}</p>
    </div>
  </div>
</template>
<script>

export default {
  name: "ShoppingCartList",
  props: ['cartItems']
}
</script>