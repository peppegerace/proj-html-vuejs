<script>
export default {
  name: 'CardReview',
  props: {
    image: String,
    title: String,
    description: String,
    name_user: String,
    job_user: String
  }
}
</script>


<template>

  <div class="col-card">

    <div class="card-review">
  
      <div class="rating">
        <i class="fa-solid fa-star"></i>
        <i class="fa-solid fa-star"></i>
        <i class="fa-solid fa-star"></i>
        <i class="fa-solid fa-star"></i>
        <i class="fa-solid fa-star"></i>
      </div>
  
      <h3>{{ title }}</h3>
  
      <p>{{ description }}</p>
  
      <div class="user">
        <div class="image">
          <img :src="image" alt="">
        </div>
        <div class="text">
          <h4>{{ name_user }}</h4>
          <span>{{ job_user }}</span>
        </div>
      </div>
  
    </div>

  </div>



</template>


<style lang="scss" scoped>
@use '../../scss/main.scss' as *;

.rating {
  color: $yellow;
}

p {
  line-height: 24px;
  margin-bottom: 20px;
  color: $grey;
  height: 140px;
  overflow: auto;
}

.col-card {
  width: 50%;
  padding: 0 10px !important;
}

.card-review {
  height: 100%;
  padding: 20px;
  color: $grey;
  background-color: $whitesmoke;

  h3 {
    margin: 20px 0;
  }

  .user {
    display: flex;
  }
  .image {
    width: 50px;
    margin-right: 20px;
    img {
      border-radius: 50%;
    }
  }
  .text {
    h4 {
      margin-bottom: 10px;
    }
    span {
      font-size: 0.8rem;
    }
  }
}


</style>