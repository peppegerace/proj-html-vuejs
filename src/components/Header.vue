<script>
export default {
  name: 'Header'
}
</script>


<template>
  
  <header>
    <div class="top-header">
      <div class="container">
        <div class="row">
          <div class="col">
            <span><i class="fa-solid fa-envelope"></i>info@example.com</span>
            <span><i class="fa-solid fa-phone"></i>+1(817)901 3377</span>
          </div>
          <div class="col">
            <nav>
              <ul>
                <li>
                  <a href="#">
                    <i class="fa-brands fa-square-facebook"></i>
                  </a>
                </li>
                <li>
                  <a href="#">
                    <i class="fa-brands fa-square-pinterest"></i>
                  </a>
                </li>
                <li>
                  <a href="#">
                    <i class="fa-brands fa-square-twitter"></i>
                  </a>
                </li>
                <li>
                  <a href="#">
                    <i class="fa-brands fa-linkedin"></i>
                  </a>
                </li>
                <li>
                  <a href="#">
                    <i class="fa-brands fa-square-instagram"></i>
                  </a>
                </li>
              </ul>
            </nav>
          </div>
        </div>
      </div>
    </div>

    <div class="bottom-header">
      <div class="container">
        <div class="row ">
          <div class="col">
            <img src="/logo.png" alt="">
          </div>
          <div class="col">
            <nav>
              <ul>
                <li>
                  <a href="#">Home</a>
                </li>
                <li>
                  <a href="#">About</a>
                </li>
                <li>
                  <a href="#">Services</a>
                </li>
                <li>
                  <a href="#">Training</a>
                </li>
                <li>
                  <a href="#">Blogs</a>
                </li>
              </ul>
              <button class="btn-custom">Get In Toch!</button>
            </nav>
          </div>
        </div>
      </div>

    </div>

  </header>

</template>


<style lang="scss" scoped>
@use '../scss/main.scss' as *;

.container {
    height: 100%;
  }
.row {
  height: 100%;
  justify-content: space-between;
  align-items: center;
  }

.top-header {
  background-color: $green;
  height: 50px;
  color: $whitesmoke;
  font-size: 0.9rem;
  span {
    margin-right: 30px;
    i {
      color: $orange;
      margin-right: 10px;
    }
  }
  nav {
    display: flex;
    height: 100%;
    align-items: center;
    li {
      display: inline-block;
      font-size: 1.4rem;
      margin-right: 10px;
    }
  }
}

.bottom-header {
  height: 100px;

  nav {
    display: flex;
    height: 100%;
    align-items: center;
    font-size: 1.3rem;
  }

  li {
    display: inline-block;
    margin-right: 40px;

    a {
      color: grey;
      &:hover {
        color: $orange;
      }
    }
  }
}
</style>