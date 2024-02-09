<template>
  <main>
    <div class="box">     
      <rating
        v-if="clicked"
        :changeRating="changeRating"
        :isSelected="isSelected"
        :isClicked="isClicked"
      >
      </rating>

      
      <thank-you
        :rating="rating"
        v-else>
      </thank-you>

    </div>
  </main>
</template>

<script>
  import Rating from "./components/Rating.vue";
  import ThankYou from "./components/ThankYou.vue";

  export default {
    components: {
      Rating,
      ThankYou
    },

    data() {
      return {
        rating: 1,
        clicked: true,
      }
    },

    methods: {
          changeRating(rate) {
            this.rating = rate;
          },
            
          isSelected(rate) {
            return this.rating === rate;
          },

          isClicked() {
            this.clicked = !this.clicked;
          }
    },

  }

</script>

<style>
  body {
    background-color: hsl(216, 12%, 8%);
    margin: 0;
    padding: 0;
    font-family: 'Overpass', sans-serif;
  }

  main {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .box {
        background-color: hsl(213, 19%, 18%);
        border-radius: 30px;
        padding: 35px 50px;
        gap: 20px;
    }

    @media (max-width: 658px) {
        .box {
          border-radius: 25px;
          padding: 25px 30px;
        }
    }


    @media (max-width: 658px) {
        .box {
          border-radius: 25px;
          padding: 23px 28px;
        }
    }

    @media (max-width: 375px) {
        .box {
          margin: 0 20px;
        }
    }
  
</style>