<template>
  <div class="sticky-top">
    <header id="site_header">
      <div class="menu ">
         <Logo/>
         <ul class="list_menu">
           <li class="active">HOME</li>
           <ListMenu :lists="lists"/>
         </ul>
      </div>
 <!-- /.menu -->
    </header>
    <!-- /#site_header -->
  </div>
</template>

<script>
import ListMenu from '../components/ListMenu.vue'
import Logo from '../components/Logo.vue'
export default {
  components: {
    ListMenu,
    Logo
  },
  data () {
    return {
      lists: ['SHOP', 'ABOUT', 'GALLERY', 'LOCATIONS', 'JOURNAL', 'CONTACT', 'MY ACCOUNT']

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
}
}

</style>
