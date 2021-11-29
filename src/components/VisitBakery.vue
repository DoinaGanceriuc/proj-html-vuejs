<template>
  <div class="col-6 bg_color_second">
      <img
        :src="require('../assets/img/' + bakeryImage)"
        :alt="bakeryPlace"
      />
      <div class="bakeries">
        <h2 class="title text-center pb-3">{{bakeryPlace}}</h2>
      <div class="bakery_info d-flex align-items-center justify-content-between">
       <div class="text-center">
      <small class="small_text">CALL US</small>
      <p>{{bakeryPhone}}</p>
       </div>
       <div class="text-center">
         <small class="small_text"> OPEN ALL WEEK</small>
          <p>{{bakeryTiming}}</p>
       </div>
      <div class="btn_first"> <a href="#"> {{bakeryAddress}}</a>
       </div>
      </div>
      </div>
      <!-- /.bakeries -->
  </div>
  <!-- /.col-6 -->
</template>

<script>
export default {
  props: {
    bakeryImage: String,
    bakeryPlace: String,
    bakeryPhone: String,
    bakeryTiming: String,
    bakeryAddress: String
  },
  data () {
    return {
      london: 'london'
    }
  }
}
</script>

<style lang="scss">
@import '../assets/scss/variables.scss';
.col-6 {
& img {
    width: 100%;
    object-fit: unset;
    height: unset;
  }
  .bakeries {
    padding: 1rem;
    .bakery_info {
      padding: 0 1rem;
      .btn_first {
        width: 100px;
      }
      p {
        font-size: 0.8rem;
      }
    }
  }
}
.bg_color_second {
    background-color: $bg_color_second;
  }
</style>
