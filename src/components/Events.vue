<template>
  <div class="row">
    <div class="col-6">
      <div class="position-relative">
      <img
        src="../assets/img/corporate-bg.jpg"
        alt="diverse persone in riunione"
      />
      <div class="info_events meeting d-flex align-items-center justify-content-center">
        <div class="events_text text-center">
          <small>INTERNATIONAL BAKERY</small>
      <h2 class="title">Corporate Events</h2>
      <div class="btn">
        <a href="#">Explore More</a>
      </div>
      </div>
      </div>
    </div>
    </div>
    <!-- ./col-6 -->
    <div class="col-6">
      <div class="position-relative">
      <img
        src="../assets/img/wedding-bg.jpg"
        alt="diverse persone in riunione"
      />
      <div class="info_events weddings d-flex align-items-center justify-content-center">
        <div class="events_text text-center">
          <small>PRIVATE DINING HALL</small>
      <h2 class="title">Weddings & Parties</h2>
      <div class="btn">
        <a href="#">Explore More</a>
      </div>
      </div>
      </div>
    </div>
    </div>
    <!-- ./col-6 -->
  </div>
   <!-- ./row-->
</template>

<script>
export default {
}
</script>

<style lang="scss">
.col-6 {
  .info_events {
    visibility: hidden;
    height: 100%;
    width: 100%;
    position: absolute;
    top: 0;
    left: 0;
    background-size: cover;
    background-repeat: no-repeat;
    color: #fff;
    h2 {
      color: #fff;
      padding: 1rem 0;
    }
    small {
      font-size: 0.5rem;
      color: #ffffffd4;
    }
  }
  .meeting {
    background-image: url('../assets/img/corporate-hover-bg.jpg');
    }
  .weddings {
    background-image: url('../assets/img/wedding-hover-bg.jpg');
    }
}
.col-6:hover .info_events{
   visibility: visible;
}
</style>
