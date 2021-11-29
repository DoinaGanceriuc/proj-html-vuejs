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
            <div class="btn_first">
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
          <h2 class="pb-5 title">
            All our delectable pastries are backed fresh in our Kitchen very
            morning, and are made with all-natural, all organi ingredients.
          </h2>
          <div class="btn">
            <a href="#">Start Shopping</a>
          </div>
        </div>
        <div class="position-relative">
          <span class="chevron left"><i class="fas fa-chevron-left"></i></span>
          <div class="row">
              <Product v-for="product in products.slice(0, 2)" :key="product.name" :productImage="product.image"
              :productName="product.name" :productPrice="product.price" :productType="product.type"/>
          </div>
          <!-- /.row -->
          <span class="chevron right"><i class="fas fa-chevron-right"></i></span>
        </div>
      </section>
      <!-- /.cookies -->
      <section class="moments container p5">
         <div class="text-center">
           <small class="small_text">CORPORATE & WEDDINGS</small>
          <h2 class="pb-5 title">
            Baking Special Moments
          </h2>
         </div>
            <Events/>
      </section>
      <!-- /.moments -->
      <section class="found_product container p5 d-flex">
        <div class="col-3 text-center pe-3 py-5">
          <h2 class="title">
            Find a freshly baked product perfect for you
          </h2>
          <p class="size_75 text_fresh_product mb-0">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos quisquam ea totam repellendus nostrum iste veniam rem hic quidem quis error, obcaecati, recusandae accusantium? Cumque sequi in dolores laboriosam maxime!</p>
          <div class="btn mt-3">
            <a href="#">Shop All Products</a>
          </div>
        </div>
        <div class="position-relative">
          <span class="chevron left"><i class="fas fa-chevron-left"></i></span>
          <div class="row">
            <FoundedProduct v-for="product in products" :key="product.name" :productImage="product.image" :productName="product.name" :productPrice="product.price"/>
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
          <div class="row py-5 ge-5 justify-content-between">
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
            <div class="col-6 pe-0">
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
      <section class="delivered container">
          <div class="row p-5">
            <div class="col-6 d-flex justify-content-between baking">
              <div class="col d-flex flex-column justify-content-between align-items-start">
                 <h2 class="fw-bold mt-2">Delivered to your home</h2>
                <div>
                <small class="small_text_bg">BAKED TO ORDER & GIFT WRAPPED</small>
                <p class="py-3 pe-5">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dolorem ipsum odit dolorum corporis omnis hic fugit accusamus. Magnam, voluptatem, consequuntur at beatae totam quis quaerat nostrum porro, dignissimos laudantium iste.</p>
              </div>
            </div>
            </div>
            <div class="col-6 d-flex justify-content-end">
                <div>
                 <p class="text_numbers fw-light">03</p>
              </div>
            </div>
          </div>
      </section>
      <!-- /.delivered -->
      <section class="locations container p5">
         <div class="text-center">
           <small class="small_text">LOCATIONS</small>
          <h2 class="pb-5 title">
            Visit our Bakeries
          </h2>
         </div>
         <div class="row gx-0">
            <VisitBakery v-for="bakery in bakeries" :key="bakery.place" :bakeryImage="bakery.image" :bakeryPlace="bakery.place" :bakeryPhone="bakery.phone" :bakeryTiming="bakery.timing" :bakeryAddress="bakery.address" :class="{bg_color_first: bakery.isActive}"/>
          </div>
          <!-- /.row -->
      </section>
      <!-- /.locations -->
      <section class="sharing container p5">
        <SocialProducts/>
      </section>
      <!-- /.sharing -->
      <section class="orders">
            <div class="container">
              <div class="col-6">
               <small class="small_text_bg">TRY OUR SEASONAL PRODUCTS</small>
              <h2 class="fw-bold">Order for pick-up or delivery to your home</h2>
              <div class="btn_first">
                <a href="#">Shop Now</a>
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
import VisitBakery from '../components/VisitBakery.vue'
import SocialProducts from '../components/SocialProducts.vue'
import Events from '../components/Events.vue'
export default {
  components: {
    Product,
    FoundedProduct,
    VisitBakery,
    SocialProducts,
    Events
  },
  data () {
    return {
      products: [
        {
          name: 'Choco Chip Cookies',
          image: 'choco-chip-cookies.jpg',
          price: '$19.00 - $39.00',
          type: 'Cookies, Patries'
        },
        {
          name: 'Strawberry Jam Cookies',
          image: 'strawberry-jam-cookies.jpg',
          price: '$24.00 - $62.00',
          type: 'Cookies, Patries'
        },
        {
          name: 'Strawberry Donut',
          image: 'strawberry-donut.jpg',
          price: '$24.00 - $42.00',
          type: 'Cookies, Patries'
        },
        {
          name: 'Perfect Macarons',
          image: 'perfect-macarons.jpg',
          price: '$18.00 - $52.00',
          type: 'Cookies, Patries'
        }
      ],
      bakeries: [
        {
          place: 'New York',
          image: 'new-york-bk.jpg',
          phone: '1.800.458.556',
          timing: '9:00 AM - 6:00 PM',
          address: 'View Map',
          isActive: true
        },
        {
          place: 'London',
          image: 'london-bk.jpg',
          phone: '1.800.458.556',
          timing: '9:00 AM - 6:00 PM',
          address: 'View Map',
          isActive: false
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
  .btn_first {
    width: 185px;
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
    background-color: $color_chrevron;
    height: 50px;
    width: 25px;
    text-align: center;
    line-height: 50px;
    color: #fff;
    z-index: 10;
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
  padding: 4rem;
  small {
    color: #99949F;
  }
}
}
.delivered {
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("../assets/img/bakery-process-3.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  color: #fff;
    h2 {
      font-size: 2.5rem;
    }
  & .col-6 {
    height: 500px;
}
}
.bg_color_first{
  background-color: $bg_color_first;
}
.orders {
  background-image: url("../assets/img/call-to-action-bg.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  color: #fff;
  .col-6 {
     padding: 5rem 0 5rem 5rem;

    h2 {
      font-size: 2.5rem;
      padding: 0.5rem 0 3rem;
 }
 .btn_first {
   width: 135px;
 }
}
}
</style>
