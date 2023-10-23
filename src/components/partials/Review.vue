<script>
import CardReview from './CardReview.vue'

export default {
  name: 'Review',
  components: {
    CardReview
  },
  data(){
    return {
      reviews: [
        {
          title: 'Great Place',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Debitis et accusamus omnis magni asperiores repellendus dignissimos maxime quidem ipsam qui tempore harum ex, excepturi deserunt.',
          image: '../../img/t1.png',
          name_user: 'Tobias May',
          job_user: 'UI/UX Designer'
        },
        {
          title: 'Beautiful Place',
          description: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dicta neque tenetur consectetur possimus recusandae dolorem at, corrupti quidem nesciunt. Consectetur quas libero quos vel laborum dolor aliquam reprehenderit dolorum debitis?',
          image: '../../img/wayne-barnett-founder-ceo.jpg',
          name_user: 'Wayne Barnett',
          job_user: 'Founder & CEO'
        },
        {
          title: 'Super!!',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi nesciunt dolor, tempore rerum velit quisquam!',
          image: '../../img/angela-caroll-chief-editor.jpg',
          name_user: 'Angela Caroll',
          job_user: 'Chief Editor'
        },
        {
          title: 'Wonderful Place',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Nemo obcaecati ratione similique maxime qui ducimus, eum minus explicabo soluta adipisci.',
          image: '../../img/walter-gordon-office-manager.jpg',
          name_user: 'Walter Gordon',
          job_user: 'Office Manager'
        },
        {
          title: 'Great Place',
          description: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Voluptates magnam autem mollitia natus debitis doloremque velit in voluptas officiis! Illum, nobis, ipsam doloribus quasi cumque autem repellendus odio dolorem ducimus quas commodi perspiciatis aliquid! Optio inventore ipsum eum voluptas, doloremque tempore aliquid, a, reiciendis quis itaque voluptatibus officia explicabo nobis.',
          image: '../../img/angela-lopez-social-media-manager.jpg',
          name_user: 'Angela Lopez',
          job_user: 'Social Media Manager'
        },
        {
          title: 'Wonderful!',
          description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. ',
          image: '../../img/scott-estrada-developer.jpg',
          name_user: 'Scott Estrada',
          job_user: 'Developer'
        },
      ],
      currentIndex: 0,
    }
  },
  methods: {

    nextReview() {
      this.currentIndex = (this.currentIndex + 1) % this.reviews.length;
    },

    prevReview() {
      this.currentIndex = (this.currentIndex - 1 + this.reviews.length) % this.reviews.length;
    }
  }
}
</script>


<template>
  <section class="review">
    <div class="container">
      <div class="row">
        <div class="col">
          <div class="card-rating">

            <div class="small-title">
              <img src="../../../img/dog-icon.png" alt="">
              <span>Review & rating</span>
            </div>
            <h2>Over 8000 Customers With 5-Star Review</h2>

            <p>It is a long established fact that a reader will be distructed by the readable content of a page when looking at its layout.</p>

            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nemo obcaecati ratione similique maxime qui ducimus, eum minus explicabo soluta adipisci.</p>

            <div class="rating">
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
            </div>
          </div>
        </div>
        <div class="card-container">
          <div class="row">
            
            <CardReview
              v-for="index in [currentIndex, (currentIndex + 1) % reviews.length]"
              :key="index"
              :image="reviews[index].image"
              :title="reviews[index].title"
              :description="reviews[index].description" 
              :name_user="reviews[index].name_user"
              :job_user="reviews[index].job_user"
            />

          </div>

          <div class="buttons">

            <button @click="prevReview"><i class="fa-solid fa-chevron-left"></i></button>
            <button @click="nextReview"><i class="fa-solid fa-chevron-right"></i></button>

          </div>

        </div>
      </div>
    </div>
  </section>
</template>


<style lang="scss" scoped>
@use '../../scss/main.scss' as *;

.review {
  padding: 80px 0;

  .col {
    width: 33%;
    height: 300px;
    padding: 0 10px;
  
    .card-rating {
      height: 100%;
      .small-title {
        display: flex;
        align-items: center;
        color: $green;
        font-weight: 500;
        margin-bottom: 20px;

        img {
          width: 30px;
          margin-right: 15px;
        }
      }

      h2 {
        margin-bottom: 20px;
        line-height: 2rem;
        font-size: 1.9rem;
        font-weight: 500;
      }

    }
  }

  .rating {
    color: $yellow;
  }

  p {
    line-height: 24px;
    margin-bottom: 20px;
    color: $grey;
  }

  .card-container {
    width: 65%;

    .buttons {
      float: right;
      button {
        background-color: $orange;
        color: $white;
        padding: 5px 10px;
        margin: 10px 10px 0 0;
        border: none;
        cursor: pointer;
        &:hover {
          background-color: $green;
        }
      }
    }
  }
}


</style>