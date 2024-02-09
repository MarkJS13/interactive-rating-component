<template>
    <div class="thankyou">
        <div class="hero">
            <img src="../assets/images/illustration-thank-you.svg" alt="">
            <p>You selected {{ rating }} out of 5 </p>
        </div>

        <div class="text-ty">
            <h1>Thank You!</h1>
            <p>We appreciate you taking the time to give a rating. <br class="remove-this"> If you ever need more support, don't hesitate <br> to get in touch! </p>
        </div>
    </div>
</template>

<script>
export default {
    props: ['rating'],
}
</script>

<style>

.thankyou {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.hero p {
    color: hsl(25, 97%, 53%);
    background-color: hsl(210, 16%, 22%);
    padding: 7px 17px;
    border-radius: 13px;
    font-size: 14px;
    margin-top: 25px;
}

.text-ty {
    text-align: center;
}

.text-ty h1 {
    color: hsl(0, 0%, 100%);
}

.text-ty p {
    color: hsl(217, 12%, 63%);
}

@media (max-width: 658px) {
    .thankyou {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .hero p {
        padding: 5px 15px;
        font-size: 12px;
    }


    .text-ty h1{
        font-size: 28px;
    }


    .text-ty p {
        font-size: 15px;
    }  
}


@media (max-width: 452px) {


    .text-ty h1{
        font-size: 25px;
    }

    .text-ty p {
        font-size: 12px;
    }  

    .remove-this {
        display: none;
    }
}

</style>