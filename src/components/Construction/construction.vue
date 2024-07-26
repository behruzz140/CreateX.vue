<template>
    <div class="container">
        <div>
            <span class="const-page-text">
                <h1 style="margin-top: 100px; font-size: 46px; color: var(--gray-900, #1E212C);
">We are Createx Construction Bureau </h1>
                <p style="margin-top: 20px; font-size: 18px; color: var(--gray-700, #808080);
">We are rightfully considered to be the best construction company in the USA.</p>
            </span>
        </div>

        <div class="const-video">
            <video src="../../assets/placeholder-video1.mp4"></video>
            <img class="play-img" src="../../assets/icons/play.svg" alt="play">
            <img class="mute-img" src="../../assets/icons/mute.svg" alt="mute">
        </div>
        <!-- aaaaaaaaaaaaaaaaaaaaaa -->
        <div class="const-part2">
            <span style="display: flex;
           flex-direction: column; align-items: center;">
                <h1>Our core values</h1>
                <p>Our mission is to set the highest standards for construction sphere.</p>
            </span>
        </div>
        <!-- bbbbbbbbbbbbbbbbb -->
        <div style="display: flex; justify-content: space-between; margin-top: 60px;">
            <div class="core-values">
                <span style="display: flex;
            align-items: center;
            flex-direction: column;"><img src="../../assets/icons/like-finger.svg" alt="like">
                    <h3>Quality</h3>
                    <p>Culpa nostrud commodo ea consequat aliquip reprehenderit. Veniam velit nostrud aliquip sunt.</p>
                </span>

            </div>

            <span style="width: 1px;
height: 188px; background-color: #808080;"></span>

            <div class="core-values">
                <span style="display: flex;
            align-items: center;
            flex-direction: column;"><img src="../../assets/icons/like-finger.svg" alt="like">
                    <h3>Safety</h3>
                    <p>Anim reprehenderit sint voluptate exercitation adipisicing laborum adipisicing. Minim empor est
                        ea.</p>
                </span>

            </div>

            <span style="width: 1px;
height: 188px; background-color: #808080;"></span>
            <div class="core-values">
                <span style="display: flex;
            align-items: center;
            flex-direction: column;"><img src="../../assets/icons/like-finger.svg" alt="like">
                    <h3>Comfort</h3>
                    <p>Sit veniam aute dolore adipisicing nulla sit culpa. Minim mollit voluptate ullamco proident ea
                        ad.</p>
                </span>

            </div>
        </div>

        
    </div>
</template>
<script>
export default {
    name: "Construction",
}
</script>
<style scoped>
.message {
    width: 414px !important;
}




.core-values>span>h3 {
    margin-top: 24px;
    margin-bottom: 8px;
    display: flex;
    width: 285px;
    height: 30px;
    flex-direction: column;
    justify-content: center;
    color: var(--gray-900, #1E212C);
    text-align: center;
    font-family: Ubuntu;
    font-size: 20px;
    font-style: normal;
    font-weight: 700;
    line-height: 150%;
    /* 30px */
}

.core-values>span>p {
    width: 285px;
    color: var(--gray-700, #808080);
    text-align: center;

    /* base/regular */
    font-family: Ubuntu;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 160%;
    /* 25.6px */
}


.const-part2>span>p {
    width: 810px;
    color: var(--gray-700, #808080);
    text-align: center;

    font-family: Ubuntu;
    font-size: 18px;
    font-style: normal;
    font-weight: 400;

}

.const-part2 {
    color: var(--gray-900, #1E212C);
    text-align: center;
    margin-top: 150px;
    /* h1 */
    font-family: Ubuntu;
    font-size: 46px;
    font-style: normal;
    font-weight: 700;
    line-height: 130%;
    /* 59.8px */
}

.const-video>.play-img {
    position: absolute;
    top: 40%;
}

.mute-img {
    position: absolute;
    width: 30px;
    height: 30px;
    bottom: -1%;
    left: 11%;
    background: #000000;
    padding: 3px;
    border-radius: 50%;
}

.const-video {
    margin-top: 90px;
    position: relative;
    width: 1230px;
    height: 500px;
    border-radius: 4px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.const-video>video {
    width: 1000px;
    height: 700px;
}

.const-page-text {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}
</style>