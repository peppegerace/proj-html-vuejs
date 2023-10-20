<script>
export default {
  name: 'Jumbotron'
}
</script>


<template>

  <div class="jumbo">

    <img src="../../img/b.png" alt="">

    <div class="container">
      <div class="welcome">
        <h1>Welcome to <span>DogMilo</span> Pets</h1>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Architecto, aliquam.</p>
        <div class="buttons">
          <button class="btn-custom">Get Started</button>
          <a href="#">
            <img src="../../img/play.png" alt="">
          </a>
        </div>
      </div>
    </div>

    <div class="chevron">
      <button>
        <i class="fa-solid fa-chevron-left"></i>
      </button>
      <button>
        <i class="fa-solid fa-chevron-right"></i>
      </button>
    </div>

  </div>

</template>


<style lang="scss" scoped>
@use '../scss/main.scss' as *;

.jumbo {
  width: 100%;
  height: 500px;
  position: relative;
  .container {
    position: relative;
    bottom: 80%;
    z-index: 99;

    .welcome {
      width: 400px;
      color: $white;
      font-size: 1.5rem;
      h1 {
        margin-bottom: 30px;
        span {
          font-weight: 400;
        }
      }
      p {
        font-size: 1.1rem;
        line-height: 1.7rem;
        margin-bottom: 30px;

      }
      .buttons {
        display: flex;
        align-items: center;
        a {
          width: 55px;
          height: 55px;
          background-color: $play;
          border-radius: 5px;
          margin-left: 15px;
          display: flex;
          justify-content: center;
          align-items: center;
        }
        img {
          width: 75%;
          height: 75%;
        }
      }
    }
  }
  .chevron {
    // width: 40px;
    // height: 40px;
    width: 100%;
    position: absolute;
    // right: 20px;
    display: flex;
    justify-content: space-between;
    bottom: 100px;
    button {
      margin: 20px;
      background: none;
      border: none;
      cursor: pointer;
      i {
        font-size: 3rem;
        color: #206dbf96;
      }
    }
  }
}

</style>