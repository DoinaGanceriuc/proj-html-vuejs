<template>
  <div class="col-6">
    <div class="position-relative">
      <img
        :src="require('../assets/img/' + productImage)"
        :alt="productName"
      />
      <div class="info_product d-flex align-items-center justify-content-center">
        <div class="product_text text-center">
      <h5 class="title">{{productName}}</h5>
      <small>{{productType}}</small>
      <p>{{productPrice}}</p>
      </div>
      </div>
        <!-- ./info_product -->
    </div>
  </div>
  <!-- ./col-6 -->
</template>

<script>
export default {
  props: {
    productImage: String,
    productName: String,
    productPrice: String,
    productType: String
  }
}
</script>

<style lang="scss">
.col-6 {
  & img {
    width: 100%;
    display: block;
    height: 100%;
    object-fit: cover;
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
    h5 {
      color: #fff;
    }
    small {
      font-size: 0.5rem;
    }
  }
}
.col-6:hover .info_product{
   visibility: visible;
}
</style>
