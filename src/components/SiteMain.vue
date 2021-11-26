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
      <section class="found_product container p5 d-flex">
        <div class="col-3 text-center align-self-center pe-4">
          <h3 class="title">
            Find a freshly baked product perfect for you
          </h3>
          <p class="size_75 text_fresh_product">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos quisquam ea totam repellendus nostrum iste veniam rem hic quidem quis error, obcaecati, recusandae accusantium? Cumque sequi in dolores laboriosam maxime!</p>
          <div class="btn">
            <a href="#">Shop All Products</a>
          </div>
        </div>
        <div class="position-relative">
          <span class="chevron left"><i class="fas fa-chevron-left"></i></span>
          <div class="row">
            <FoundedProduct v-for="product in foundedProducts" :key="product.name" :productImage="product.image" :productName="product.name" :productPrice="product.price"/>
          </div>
          <!-- /.row -->
          <span class="chevron right"><i class="fas fa-chevron-right"></i></span>
        </div>

      </section>
      <!-- /.found_product -->
      <section class="opinions container">
          <div class="row p-5">
            <div class="col-6 pr_6">
              <h2 class="fw-bold">Tell us what you have in mind</h2>
            </div>
            <div class="col-6 d-flex flex-column justify-content-between align-items-end">
              <div>
                 <p class="text_numbers fw-light">01</p>
              </div>
                <div>
                <small class="small_text_bg">MANUAL INGREDIENTS SELECTION</small>
                <p class="pt-3">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolorem ipsum odit dolorum corporis omnis hic fugit accusamus. Magnam, voluptatem, consequuntur at beatae totam quis quaerat nostrum porro, dignissimos laudantium iste.</p>
              </div>
            </div>
          </div>
      </section>
      <!-- /.opinions -->
      <section class="mass_produced">
        <div class="container">
          <div class="row p-5 justify-content-between">
            <div class="col-6 d-flex justify-content-between baking p-5">
              <div class="col-8 d-flex flex-column justify-content-between align-items-start">
                 <h2 class="fw-bold mt-2">We Start Baking</h2>
                <div>
                <small class="small_text_bg">SWEET & DELICIOUS</small>
                <p class="pt-3">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolorem ipsum odit dolorum corporis omnis hic fugit accusamus. Magnam, voluptatem, consequuntur at beatae totam quis quaerat nostrum porro, dignissimos laudantium iste.</p>
              </div>
            </div>
              <div>
                 <p class="text_numbers fw-light">02</p>
              </div>
            </div>
            <div class="col-6">
              <div class="bg_founder">
                <small class="small_text_bg">DONT JUST TAKE OUR WORD FOR IT</small>
                <h2 class=" title">"Finally found an alternative to the mass produced products. Something that incorporates real organic ingredients, nutrient dense wellness while promoting sustainability and activity."</h2>
                 <small class="small_text_bg">Rachel Cooper, Founder</small>
              </div>
            </div>
          </div>
        </div>
      </section>
      <!-- /.mass_produced -->
      <section class="opinions">
        <div class="container">
          <div class="row p-5">
            <div class="col-6 pr_6">
              <h2 class="fw-bold">Tell us what you have in mind</h2>
            </div>
            <div class="col-6 d-flex flex-column justify-content-between align-items-end">
              <div>
                 <p class="text_numbers fw-light">01</p>
              </div>
                <div>
                <small class="small_text_bg">MANUAL INGREDIENTS SELECTION</small>
                <p class="pt-3">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolorem ipsum odit dolorum corporis omnis hic fugit accusamus. Magnam, voluptatem, consequuntur at beatae totam quis quaerat nostrum porro, dignissimos laudantium iste.</p>
              </div>
            </div>
          </div>
        </div>
      </section>
      <!-- /.opinions -->
    </main>
    <!-- /#site_main -->
  </div>
</template>

<script>
import Product from '../components/Product.vue'
import FoundedProduct from '../components/FoundedProduct.vue'
export default {
  components: {
    Product,
    FoundedProduct
  },
  data () {
    return {
      ListNumbersCol: [6, 3],
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
      ],
      foundedProducts: [
        {
          name: 'Choco Chip Cookies',
          image: 'choco-chip-cookies.jpg',
          price: '$19.00 - $39.00'
        },
        {
          name: 'Strawberry Jam Cookies',
          image: 'strawberry-jam-cookies.jpg',
          price: '$24.00 - $62.00'
        },
        {
          name: 'Strawberry Donut',
          image: 'strawberry-donut.jpg',
          price: '$24.00 - $42.00'
        },
        {
          name: 'Perfect Macarons',
          image: 'perfect-macarons.jpg',
          price: '$18.00 - $52.00'
        }
      ]
    }
  }
}

</script>

<style lang="scss">
@import '../assets/scss/variables.scss';
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
.text_fresh_product {
  color: $color_small;
}
.opinions {
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("../assets/img/bakery-process-1.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  color: #fff;
  // background-position: center;
  .col-6 {
    height: 500px;
    h2 {
      font-size: 2.5rem;
    }
  }
}
.mass_produced {
   .col-6 {
    height: 500px;
}
.baking {
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("../assets/img/bakery-process-2.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  color: #fff;
    h2 {
      font-size: 2.5rem;
    }
}
.bg_founder {
  background-color: #F1EDF5;
  height: 100%;
  padding: 5rem;
  small {
    color: #99949F;
  }
}
}
</style>
