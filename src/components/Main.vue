<script>
import AboutUs from './partials/AboutUs.vue';
import Service from './partials/Service.vue';

export default {
  name: 'Main',
  components: {
    AboutUs,
    Service
  }
}
</script>


<template>
  
  <main>

    <!-- <section class="about-us">
      
      <div class="container">
        <div class="row">

          <div class="col">
            <img src="../../img/about.png" alt="">
          </div>

          <div class="col">
            <div class="small-title">
              <img src="../../img/dog-icon.png" alt="">
              <span>About Us</span>
            </div>
            <h2>Welcome DogMilo Pets</h2>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Delectus, eaque, non tempore perferendis dicta at accusamus ipsum dolore quisquam quo quis a, ad voluptates explicabo soluta amet aliquam doloribus rem!</p>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Delectus, eaque, non tempore perferendis dicta at accusamus ipsum dolore quisquam quo quis a, ad voluptates explicabo soluta amet aliquam doloribus rem!</p>
          </div>

        </div>
      </div>
      
    </section> -->

    <AboutUs />
    <Service />
   

    <section class="choose-us">
      
    </section>


    <section class="review">
      
    </section>

  </main>

</template>


<style lang="scss">
@use '../scss/main.scss' as *;



</style>