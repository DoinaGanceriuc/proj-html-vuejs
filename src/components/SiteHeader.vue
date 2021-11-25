<template>
  <div>
    <header id="site_header">
      <div class="menu">
         <div class="logo">
        <img src="../assets/img/avada-bakery-logo.png" alt="logo baker purple" width="125"/>
      </div>
      <!-- /.logo -->
         <ListMenu :lists="lists"/>
      </div>
          <div class="container">
            <section class="text_jumbo">
              <small>FRESH & TASTY BAKERY EVERY DAY</small>
              <h1>The Perfect Fresh Bread</h1>
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati pariatur iure officiis, excepturi nemo laborum ipsam explicabo non animi minus commodi impedit facere. Impedit explicabo esse numquam accusamus nostrum quae?</p>
              <div class="btn">
                <a href="#">Explore our products</a>
              </div>
            </section>
        </div>
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
  background-image: url("../assets/img/hero-header-bakery.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  .menu {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 3rem 1rem;
/* logo */
.logo {
  padding-bottom: 1rem;
}
}
.text_jumbo {
  max-width: 330px;
  padding: 6rem 0 9rem 0;
  & small {
    color: #8C8693;
    font-size: 0.5rem;
  }
  & h1 {
    padding-top: 1rem;
    color: #614093;
    font-size: 2rem;
  }
  & p {
    padding: 2rem 0;
    color: #8C8693;
    font-size: 0.8rem;
  }
  & .btn {
    background-color: #fff ;
    padding: 0.8rem 1.5rem;
    text-align: center;
    font-size: 0.8rem;
    border: none;
    width: 185px;
    border-radius: 5px;
    & a {
      text-decoration: none;
      color: #614093;
    }
  }
}
}

</style>
