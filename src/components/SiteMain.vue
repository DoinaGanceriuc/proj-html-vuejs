<template>
  <div>
    <main id="site_main">
      <div class="jumbotron">
        <div class="container">
        <section class="text_jumbo">
          <small>FRESH & TASTY BAKERY EVERY DAY</small>
          <h1>The Perfect Fresh Bread</h1>
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
    </main>
    <!-- /#site_main -->
  </div>
</template>

<script></script>

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
  & small {
    color: #8C8693;
    font-size: 0.5rem;
  }
  & h1 {
    padding-top: 1rem;
    color: #614093;
    font-size: 2.5rem;
    font-weight: 700;
  }
  & p {
    padding: 2rem 0;
    color: #8C8693;
    font-size: 0.75rem;
  }
  & .btn {
    background-color: #fff ;
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
  </style>
