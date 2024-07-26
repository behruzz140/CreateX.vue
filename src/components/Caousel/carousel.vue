<template>
    <div class="carousel-img">
        <div class="text-carousel">
            <span class="carousel-h1">
                <h1 style="display: flex; align-items: center; gap: 5px;">CREATE <p
                        style="color: #FF5A30; font-size: 90px;">X</p>
                </h1>
                <h1> CONSTRUCTION</h1>
            </span>
            <p class="carousel-p">Cras ultrices leo vitae non viverra. Fringilla nisi quisque consequat, dignissim vitae
                proin ipsum sed.
                Pellentesque nec turpis purus eget pellentesque integer ipsum elementum felis. </p>

            <div class="carousel-btns">
                <span>
                    <p class="learnMore">Learn more about us</p>
                </span>
                <span>
                    <button class="submitBtn">SUBMIT REQUEST</button>
                </span>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'CrouselPage'
}
</script>
<style scoped>
.text-carousel {
    position: absolute;
    top: 40%;
    left: 15%;
}

.carousel-btns {
    display: flex;
    align-self: center;
    gap: 24px;
    margin-top: 61px;
}

.submitBtn {
    color: var(--white, #FFF);
    text-align: center;
    font-family: Ubuntu;
    font-size: 16px;
    font-style: normal;
    font-weight: 700;
    line-height: 52px;
    /* 325% */
    letter-spacing: 0.5px;
    text-transform: uppercase;
    display: flex;
    padding: 0px 40px;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    border-radius: 4px;
    background: var(--primary, #FF5A30);
}

.learnMore {
    color: var(--white, #FFF);
    text-align: center;
    font-family: Ubuntu;
    font-size: 16px;
    font-style: normal;
    font-weight: 700;
    line-height: 52px;
    letter-spacing: 0.5px;
    text-transform: uppercase;
    display: flex;
    padding: 0px 40px;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    border-radius: 4px;
    border: 1px solid var(--white, #FFF);
}

.carousel-img {
    background-image: url(../../assets//images/bg-image.png);
    height: 788px;
}

.carousel-h1 {
    display: flex;
    flex-direction: column;
    color: #fff;

    font-family: Ubuntu;
    font-size: 72px;
    font-style: normal;
    font-weight: 700;
    line-height: 130%;
    letter-spacing: 1px;
}

.carousel-p {
    width: 595px;
    color: var(--white, #FFF);
    font-family: Ubuntu;
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    margin-top: 24px;
}
</style>