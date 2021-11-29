<template>
  <div>
    <ul class="list_menu">
       <li v-for="list in lists" :key="list">{{list}}</li>
       <li class="shop"><i class="fas fa-shopping-cart"></i></li>
    </ul>

  </div>
</template>

<script>
export default {
  props: {
    lists: Array
  }
}
</script>

<style lang="scss">
@import '../assets/scss/variables.scss';
.list_menu {
  display: flex;
  list-style: none;
  padding: 0;
  li {
    padding-right: 2rem;
    font-size: 0.5rem;
    color: $color_primary;
  }
   .shop {
      padding: 0 0.5rem;
    }
  .active {
      color: $color_primary;
      &::after {
        content: "";
        display: block;
        width: 30px;
        height: 2px;
        background-color: $color_primary;
        margin: auto;
        margin-top: 5px;
      }
    }
}
</style>
