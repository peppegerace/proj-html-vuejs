<script>
export default {
  name: 'Subscribe'
}
</script>


<template>
  <div class="container">

    <div class="subscribe">

      <div class="left">
        <img src="../../../img/news.png" alt="">
      </div>

      <div class="right">
        <h2>Subscribe to Our Newslatter</h2>

        <div class="mail">

          <input type="text" placeholder="Your Email Here">
          <button><i class="fa-solid fa-at"></i></button>

        </div>
      </div>
    </div>

  </div>
</template>



<style lang="scss" scoped>
@use '../../scss/main.scss' as *;


.subscribe {
  position: relative;
  top: 100px;
  width: 960px;
  height: 200px;
  background-color: $orange;
  margin: 0 auto;
  border-radius: 10px;
}
.left {
  float: left;
  width: 50%;
  
  img {
    width: 350px;
    position: relative;
    bottom: 103px;
    left: 40px;
  
  }
}

.right {
  float: right;
  width: 50%;
  color: $white;
  padding: 50px 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;

  h2 {
    margin-bottom: 20px;
  }

  .mail {
    width: 100%;
    height: 50px;
    padding: 2px;
    background-color: $white;
  }
  input {
    width: calc(100% - 40px);
    height: 100%;
    padding: 20px;
    border: none;
  }
  button {
    width: 40px;
    height: 100%;
    background-color: $orange;
    color: $white;
    border: 1px solid $white;
    cursor: pointer;
  }
}
</style>