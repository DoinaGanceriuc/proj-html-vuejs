<template>
  <div class="col-3">
    <div class="position-relative">
      <img
        :src="require('../assets/img/' + productImage)"
        :alt="productName"
      />
      <div class="info_product d-flex align-items-center justify-content-center">
        <p>SELECT OPTIONS / QUICK VIEW</p>
      </div>
    </div>
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
 .info_product {
    visibility: hidden;
    height: 100%;
    width: 100%;
    position: absolute;
    top: 0;
    left: 0;
    background-color: #00000075;
    color: #fff;
    p {
      font-size: 0.9rem;
      padding: 1rem;
    }
  }
.col-3:hover .info_product{
   visibility: visible;
}
</style>
