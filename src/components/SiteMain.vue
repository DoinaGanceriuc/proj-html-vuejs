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
      <section class="cookies container d-flex">
        <div class="col-4">
          <small>OUR PRODUCTS</small>
          <h2 class="pb-5">
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
            <div class="col-6">
              <img
                src="../assets/img/choco-chip-cookies.jpg"
                alt="logo baker purple"
                width=""
              />
            </div>
            <div class="col-6">
              <img
                src="../assets/img/strawberry-jam-cookies.jpg"
                alt="logo baker purple"
                width=""
              />
            </div>
          </div>
          <!-- /.row -->
          <span class="chevron right"><i class="fas fa-chevron-right"></i></span>
        </div>
      </section>
      <!-- /.cookies -->
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
    color: #8c8693;
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
  padding: 5rem 0;
  & small {
    color: #8c8693;
    font-size: 0.5rem;
  }
  & h2 {
    padding-top: 1rem;
    color: #614093;
    font-weight: 600;
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
.col-6 {
  & img {
    width: 100%;
    display: block;
    height: 100%;
    object-fit: cover;
  }
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
