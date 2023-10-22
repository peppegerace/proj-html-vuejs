<script>
import CardService from './CardService.vue'

export default {
  name: 'Service',
  components: {
    CardService
  },
  data(){
    return {
      services: [
        {
          image: '../../img/d-1.png',
          title: 'Pet Sitting',
          description: 'The readable content of a page when looking at its layout.'
        },
        {
          image: '../../img/d-2.png',
          title: 'Puppy Sitting',
          description: 'The readable content of a page when looking at its layout.'
        },
        {
          image: '../../img/d-3.png',
          title: 'Dog Walking',
          description: 'The readable content of a page when looking at its layout.'
        },
        {
          image: '../../img/d-4.png',
          title: 'Night Care',
          description: 'The readable content of a page when looking at its layout.'
        },
        {
          image: '../../img/d-5.png',
          title: 'Pet Sitting',
          description: 'The readable content of a page when looking at its layout.'
        }
      ]
    }
  }
}
</script>


<template>
  <section class="service">

    <div class="title">
      <h5>Service</h5>
      <h2>DogMilo Pet Care Services <br> For Your Best Friends.</h2>
    </div>

    <div class="container">
      <div class="row">
        <CardService
          v-for="service in services"
          :key="service"
          :image="service.image"
          :title="service.title"
          :description="service.description" />
      </div>
    </div>

  </section>
</template>


<style lang="scss" scoped>
@use '../../scss/main.scss' as *;

.service {
  // height: 300px;
  padding: 50px 0;
  position: relative;
  background-color: $whitesmoke;

  &::before,
  &::after {
    content: "";
    position: absolute;
    top: 0;
    bottom: 0;
    width: 50%;
    background-size: 200px;
    background-repeat: no-repeat;
  }
  &::before {
    background-image: url(../../../img/dog-left.png);
    background-position: left;
  }
  &::after {
    right: 0;
    background-image: url(../../../img/dog-logo.png);
    background-position: right;
  }
  .title {
    width: 35%;
    margin: 0 auto;
    text-align: center;

    h5 {
      color: $green;
      margin-bottom: 30px;
    }

    h2 {
      font-weight: 400;
      margin-bottom: 30px;
    }
  }
  .row {
  justify-content: space-between;
  }
}


</style>