<template>
  <div>
    <main id="site_main">
      <div class="jumbotron">
        <div class="container">
          <section class="text_jumbo">
            <small class="small_text">FRESH & TASTY BAKERY EVERY DAY</small>
            <h1 class="title">The Perfect Fresh Bread</h1>
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Obcaecati
              pariatur iure officiis, excepturi nemo laborum ipsam explicabo non
              animi minus commodi impedit facere. Impedit explicabo esse numquam
              accusamus nostrum quae?
            </p>
            <div class="btn">
              <a href="#">Explore our products</a>
            </div>
          </section>
        </div>
        <!-- /.container -->
      </div>
      <!-- /.jumbotron -->
      <section class="cookies container d-flex p5">
        <div class="col-4">
          <small class="small_text">OUR PRODUCTS</small>
          <h3 class="pb-5 title">
            All our delectable pastries are backed fresh in our Kitchen very
            morning, and are made with all-natural, all organi ingredients.
          </h3>
          <div class="btn">
            <a href="#">Start Shopping</a>
          </div>
        </div>
        <div class="position-relative">
          <span class="chevron left"><i class="fas fa-chevron-left"></i></span>
          <div class="row">
            <Product v-for="product in products" :key="product.name" :productImage="product.image"/>
          </div>
          <!-- /.row -->
          <span class="chevron right"><i class="fas fa-chevron-right"></i></span>
        </div>
      </section>
      <!-- /.cookies -->
      <section class="moments container p5">
         <div class="text-center">
           <small class="small_text">CORPORATE & WEDDINGS</small>
          <h3 class="pb-5 title">
            Baking Special Moments
          </h3>
         </div>
         <div class="row">
            <Product v-for="product in events" :key="product.name" :productImage="product.image"/>
          </div>
          <!-- /.row -->
      </section>
      <!-- /.moments -->
    </main>
    <!-- /#site_main -->
  </div>
</template>

<script>
import Product from '../components/Product.vue'
export default {
  components: {
    Product
  },
  data () {
    return {
      products: [
        {
          name: 'choco cookies',
          image: 'choco-chip-cookies.jpg'
        },
        {
          name: 'strawberry cookies',
          image: 'strawberry-jam-cookies.jpg'
        }
      ],
      events: [
        {
          name: 'corporate',
          image: 'corporate-bg.jpg'
        },
        {
          name: 'wedding',
          image: 'wedding-bg.jpg'
        }
      ]

    }
  }
}

</script>

<style lang="scss">
.jumbotron {
  background-image: url("../assets/img/hero-header-bakery.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}
.text_jumbo {
  max-width: 330px;
  padding: 9rem 0 9rem 0;
  & h1 {
    font-size: 2.5rem;
  }
  & p {
    padding: 2rem 0;
    color: #8c8693;
    font-size: 0.75rem;
  }
  & .btn {
    background-color: #fff;
    padding: 0.8rem 1.5rem;
    text-align: center;
    font-size: 0.75rem;
    border: none;
    width: 185px;
    border-radius: 5px;
    & a {
      text-decoration: none;
      color: #614093;
    }
  }
}
.cookies {
  & h3 {
    font-size: 1.75rem;
  }
  & .btn {
    background-color: #55328b;
    padding: 0.75rem 0.5rem;
    text-align: center;
    font-size: 0.75rem;
    border: none;
    width: 135px;
    border-radius: 5px;
    & a {
      text-decoration: none;
      color: #fff;
    }
  }
}
.col-4 {
  padding: 0rem 1rem;
}
.chevron {
    position: absolute;
    background-color: #A691B2;
    height: 50px;
    width: 25px;
    text-align: center;
    line-height: 50px;
    color: #fff;
  &.left {
    left: 0;
    top: 50%;
  }
  &.right {
    right: 0;
    top: 50%;
  }
}
</style>
