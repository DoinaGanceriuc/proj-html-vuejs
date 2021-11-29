<template>
  <div class="col-3">
      <img
        :src="require('../assets/img/' + productImage)"
        :alt="productName"
      />
      <div class="text-center product_text">
      <h5 class="title">{{productName}}</h5>
      <p>{{productPrice}}</p>
      </div>
  </div>
</template>

<script>
export default {
  props: {
    productImage: String,
    productName: String,
    productPrice: String
  }
}
</script>

<style lang="scss">
@import '../assets/scss/variables.scss';
.col-3 {
  & img {
    width: 100%;
    display: block;
    height: 90%;
    object-fit: cover;
  }
  .product_text {
    color: $color_primary;
    font-size: 0.9rem
  }
}
</style>
