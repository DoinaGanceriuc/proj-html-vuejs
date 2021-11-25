<template>
  <div>
    <header id="site_header">
      <div class="menu fixed-top">
         <div class="logo">
        <img src="../assets/img/avada-bakery-logo.png" alt="logo baker purple" width="125"/>
      </div>
      <!-- /.logo -->
         <ListMenu :lists="lists"/>
      </div>
 <!-- /.menu -->
    </header>
    <!-- /#site_header -->
  </div>
</template>

<script>
import ListMenu from '../components/ListMenu.vue'
export default {
  components: {
    ListMenu
  },
  data () {
    return {
      lists: ['shop', 'about', 'gallery', 'locations', 'journal', 'contact', 'my account']

    }
  }
}

</script>

<style lang="scss">
#site_header {
  background-color: #F5E9F3;
  .menu {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem;
/* logo */
.logo {
  padding-bottom: 1rem;
}
}
}

</style>
