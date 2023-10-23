<script>
import AboutUs from './partials/AboutUs.vue';
import Service from './partials/Service.vue';
import ChooseUs from './partials/ChooseUs.vue';
import Review from './partials/Review.vue';

export default {
  name: 'Main',
  components: {
    AboutUs,
    Service,
    ChooseUs,
    Review
  }
}
</script>


<template>
  
  <main>

    <AboutUs />
    <Service />
    <ChooseUs />
    <Review />

  </main>

</template>


<style lang="scss">
@use '../scss/main.scss' as *;



</style>