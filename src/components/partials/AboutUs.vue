<script>
export default {
  name: 'AboutUs'
}
</script>


<template>

  <section class="about-us">
      
      <div class="container">
        <div class="row">

          <div class="col">
            <img src="../../../img/about.png" alt="">
          </div>

          <div class="col">
            <div class="small-title">
              <img src="../../../img/dog-icon.png" alt="">
              <span>About Us</span>
            </div>
            <h2>Welcome DogMilo Pets</h2>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Delectus, eaque, non tempore perferendis dicta at accusamus ipsum dolore quisquam quo quis a, ad voluptates explicabo soluta amet aliquam doloribus rem!</p>
            <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Delectus, eaque, non tempore perferendis dicta at accusamus ipsum dolore quisquam quo quis a, ad voluptates explicabo soluta amet aliquam doloribus rem!</p>
          </div>

        </div>
      </div>
      
    </section>

</template>


<style lang="scss">
@use '../../scss/main.scss' as *;


.about-us {
  // margin: 100px auto;
  background-image: url(../../../img/dog-logo.png);
  background-repeat: no-repeat;
  background-size: 200px;
  background-position: right;

  .container {
    padding: 100px 0;
    .row {
      .col:first-child {
        width: 40%;
      }
  
      .col:last-child {
        width: 60%;
        padding: 80px 100px;
        .small-title {
          display: flex;
          align-items: center;
          color: $green;
          font-weight: 500;
          margin-bottom: 30px;
          img {
            width: 40px;
            margin-right: 20px;
          }
        }
        h2 {
          font-size: 2.5rem;
          font-weight: 500;
          margin-bottom: 30px;
        }
        p {
          color: $grey;
          margin-bottom: 20px;
          line-height: 25px;
        }
      }
    }
  }
}

</style>