<template>
  <div class="col-6" >
      <img
        :src="require('../assets/img/' + productImage)"
        :alt="productName"
      />
  </div>
</template>

<script>
export default {
  props: {
    productImage: String,
    productName: String
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
}
</style>
