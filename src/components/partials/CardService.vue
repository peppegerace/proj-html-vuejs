<script>
export default {
  name: 'CardService',
  props: {
    image: String,
    title: String,
    description: String
  }
}
</script>


<template>

  <div class="col">
    
    <div class="card">
  
      <img :src="image" alt="">
      <h4>{{ title }}</h4>
      <p>{{ description }}</p>
      <a href="#">
        <i class="fa-solid fa-chevron-right"></i>
      </a>
    </div>
    

  </div>

</template>



<style lang="scss" scoped>
@use '../../scss/main.scss' as *;

.col {
  width: calc(100% / 5);
}

.card {
  margin: 0 auto;
  width: 85%;
  background-color: $orange;
  color: $white;
  border-top-left-radius: 100px;
  border-top-right-radius: 100px;
  border-bottom-left-radius: 100px;
  border-bottom-right-radius: 100px;
  padding: 20px;
  display: flex;
  align-items: center;
  flex-direction: column;
  
  &:hover {
    background-color: $green !important;
  }

  img {
    width: 60px;
    height: 60px;
    margin-bottom: 20px;
  }

  h4,
  p {
    margin-bottom: 20px;
  }

  p {
    line-height: 24px;
  }

  a {
    padding: 15px 20px;
    border-radius: 50%;
    background-color: $yellow;
    &:hover {
      cursor: pointer;
    }

    i {
      color: black;
      font-size: 1.5rem;
    }
  }
}
</style>