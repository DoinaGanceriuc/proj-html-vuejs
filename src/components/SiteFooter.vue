<template>
  <div>
    <footer id="site_footer" class="container p-0">
      <div class="menu pt-5 d-flex justify-content-between">
         <Logo/>
         <div class="subscribe text-end">
         <h5 class="title pb-4">Subscribe to our Newsletter</h5>
         <input type="email" placeholder="Enter email address*" class="">
         <div class="btn">
           <a href="#">Subscribe</a>
         </div>
      </div>
      </div>
      <ul class="d-flex align-items-center py-3 px-0">
          <ListMenu :lists="lists"/>
         <li class="number_orders">0</li>
      </ul>
      <div class="copyright d-flex justify-content-between">
        <div class="copyright_text">
           <small class="small_text">
          <i class="far fa-copyright"></i>
          Copyright 2012 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress
        </small>
        </div>
        <div class="icons_socials">
          <i class="fab fa-instagram"></i>
          <i class="fab fa-twitter"></i>
          <i class="fab fa-facebook-f"></i>
          <i class="fab fa-pinterest-p"></i>
        </div>
      </div>
      <!-- /.copyright -->
    </footer>
    <!-- /#site_footer -->
  </div>
</template>

<script>
import ListMenu from '../components/ListMenu.vue'
import Logo from '../components/Logo.vue'
export default {
  components: {
    Logo,
    ListMenu
  },
  data () {
    return {
      lists: ['Shop', 'About', 'Gallery', 'Locations', 'Journal', 'Contact', 'Orders']

    }
  }
}

</script>

<style lang="scss">
@import '../assets/scss/variables.scss';
ul {
  list-style: none;
   li {
    font-size: 0.5rem;
    color: $color_primary;
  }
  .number_orders {
    height: 15px;
    width: 15px;
    background-color: #F0EDF5;
    border-radius: 50%;
    text-align: center;
  }
}
.subscribe {
  input {
    padding: 0.4rem 5rem 0.5rem 0.5rem;
    border-radius: 5px;
    border: 1px solid #F6F6F7;
    margin-right: 1rem;
    font-size: 0.9rem;

  }
  .btn {
    padding: 0.6rem 0.5rem;
  }
}
.copyright{
  padding: 3rem 0;
.icons_socials {
  i {
    color: $color_primary;
    padding: 0 1rem;
  }
  }
}
</style>
