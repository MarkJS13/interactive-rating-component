<template>
      <div class="star">
        <img src="../assets/images/icon-star.svg" alt="icon">
      </div>

      <div class="text">
        <h1> How did we do? </h1>
        <p>Please let us know how we did with your support <br class="remove-this"> request. All feedback is appreciated to help us <br class="remove-this"> improve our offering! </p>
      </div>

      <div class="form">
        <div class="radioBtn">
            <p
            @click="changeRating_(1)" :class="{'selected': isSelected_(1)}">1</p>
            <p
            @click="changeRating_(2)" :class="{'selected': isSelected_(2)}">2</p>
            <p
            @click="changeRating_(3)" :class="{'selected': isSelected_(3)}">3</p>
            <p
            @click="changeRating_(4)" :class="{'selected': isSelected_(4)}">4</p>
            <p
            @click="changeRating_(5)" :class="{'selected': isSelected_(5)}">5</p>    
        </div>
        <button type="submit" @click="isClicked_">
            Submit
        </button>
      </div>

</template>

<script>

    export default {

        props: ['changeRating', 'isSelected', 'isClicked'],

        methods: {
            changeRating_(rate) {
                this.changeRating(rate);
            },

            
            isSelected_(rate) {
                return this.isSelected(rate);
            },

            isClicked_() {
                this.isClicked();
            }

            

        },

    }

</script>

<style>
    
    .star img{
        padding: 10px;
        background-color: hsl(210, 16%, 22%);
        border-radius: 40px;
    }

    .text h1{
        color: hsl(0, 0%, 100%);
        font-weight: 500;
    }

    .text p{
        color: hsl(217, 12%, 63%);
        line-height: 1.5;
    }

    .form {
        display: flex;
        flex-direction: column;
        gap: 10px;
    }

    .form .radioBtn {
        display: grid;
        grid-auto-flow: column;
        gap: 20px;
    }

    .form .radioBtn p {
        background-color: hsl(210, 16%, 22%);
        color: hsl(217, 12%, 63%);
        padding: 15px;
        border-radius: 50%;
        font-size: 15px;
        font-weight: 500;
        text-align: center;
    }

    .selected {
        background-color: hsl(216, 12%, 54%) !important;
        color: hsl(0, 0%, 100%) !important;
    }

    .form .radioBtn p:hover {
        background-color: hsl(25, 97%, 53%);
        color: hsl(0, 0%, 100%);
        transition: .8s;
        cursor: pointer;
    }

    .form button {
        background-color: hsl(25, 97%, 53%);
        border: none;
        color: hsl(0, 0%, 100%);
        padding: 13px;
        border-radius: 25px;
        text-transform:  uppercase;
        font-size: 14px;
        font-weight: 600;
        letter-spacing: 2px;
    }

    .form button:hover {
        color: hsl(25, 97%, 53%);
        background-color: hsl(0, 0%, 100%);
        cursor: pointer;
        transition: .8s;
    }

    @media (max-width: 658px) {

        .text h1{
            font-size: 28px;
        }

        .text p{
            font-size: 15px;
        }

        .form {
            gap: 8px;
        }

        .form .radioBtn {
            gap: 25px;
        }

        .form .radioBtn p {
            padding: 10px;
            font-size: 15px;
        }

        .form button {
            padding: 13px;
            font-size: 13px;
        }
    }

    @media (max-width: 452px) {
        .text {
            text-align: start;
        }

        .text h1{
            font-size: 26px;
            text-align: start;
        }

        .text p{
            font-size: 13px;
            text-align: start;
        }

        .form {
            gap: 6px;
        }

        .form .radioBtn {
            gap: 20px;
        }

        .form .radioBtn p {
            padding: 10px;
            font-size: 15px;
        }

        .form button {
            padding: 12px;
            font-size: 12px;
        }
    }

        @media (max-width: 375px) {
        .remove-this {
          display: none;
        }
    }




</style>