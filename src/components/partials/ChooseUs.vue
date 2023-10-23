<script>
export default {
  name: 'ChooseUs'
}

</script>


<template>

  <section class="choose-us">

    <div class="choose-left">
      <img src="../../../img/why.png" alt="">
    </div>

    <div class="choose-right">

      <div class="small-title">
        <img src="../../../img/dog-icon.png" alt="">
        <span>Choose Us</span>
      </div>
      <h2>Why Choose Us?</h2>

      <ul>
        <li>
          <div class="image">
            <img src="../../../img/w-3.png" alt="">
          </div>
          <div class="text">
            <h3>Safety First</h3>
            <p>It is a long established fact that a reader will be distructed by the readable content of a page when looking at its layout.</p>
          </div>
        </li>

        <li class="li-mid">
          <div class="image">
            <img src="../../../img/w-2.png" alt="">
          </div>
          <div class="text">
            <h3>Safety First</h3>
            <p>It is a long established fact that a reader will be distructed by the readable content of a page when looking at its layout.</p>
          </div>
        </li>

        <li class="li-end">
          <div class="image">
            <img src="../../../img/w-1.png" alt="">
          </div>
          <div class="text">
            <h3>Safety First</h3>
            <p>It is a long established fact that a reader will be distructed by the readable content of a page when looking at its layout.</p>
          </div>
        </li>
      </ul>
    </div>
      
  </section>
  
</template>


<style lang="scss" scoped>
@use '../../scss/main.scss' as *;

.choose-us {
  display: flex;
  color: $grey;

  .choose-left {
    width: 47%;
  }

  .choose-right {
    padding: 50px;

    .small-title {
      display: flex;
      align-items: center;
      color: $green;
      font-weight: 500;
      margin-bottom: 20px;

      img {
        width: 70px;
        margin-right: 20px;
      }
      
    }

    h2 {
      font-size: 2rem;
      margin-bottom: 30px;
    }

    li {
      display: flex;
    }
    .image {
      width: 130px;
      margin-right: 30px;
    }

    .text {
      p {
        margin: 20px 0;
        line-height: 24px;

      }
    }

    .li-mid {
      position: relative;
      left: 20%;
      .text {
        width: 58%;
      }
    }

    .li-end {
      position: relative;
      left: 40%;
      .text {
        width: 37%;
      }
    }
    
  }
}

</style>