<template>
    <div class="main-partners">
        <div class="container">
            <div>
                <h2 class="partners-h2">Supported by 12+ partners</h2>
            </div>
            <div class="InDepth">
                <img src="../../assets/images/InDepth.png" alt="Indepth">
                <img src="../../assets/images/higherFit.png" alt="Indepth">
                <img src="../../assets/images/sential.png" alt="Indepth">
                <img src="../../assets/images/HappyHome.png" alt="Indepth">
                <img src="../../assets/images/ForSale.png" alt="Indepth">
                <img src="../../assets/images/Sunset.png" alt="Indepth">

            </div>

            <div class="client-saying">

                <div class="edwards">
                    <h2>What our clients are saying</h2>
                    <img src="../../assets/images/profile-image.png" alt="ProfileImg">
                    <p class="edwards-p1">Ipsum aute sunt aliquip aute et occaecat. Anim minim do cillum eiusmod enim.
                        Consectetur magna cillum
                        consequat minim laboris cillum laboris voluptate minim proident exercitation ullamco. </p>
                    <h3>Shawn Edwards</h3>
                    <div class="company-name">
                        <p class="edwards-p2">Position, Company name</p>
                        <span class="arrows-btn">
                            <button><img src="../../assets/icons/left-2.svg" alt="left"></button>
                            <button><img src="../../assets/icons/right-2.svg" alt="right"></button>
                        </span>
                    </div>
                </div>
                <div class="partners-worker">

                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: "Partners",
}
</script>
<style scoped>
h2 {
    color: var(--gray-900, #1E212C);
    text-align: center;

    /* h1 */
    font-family: Ubuntu;
    font-size: 46px;
    font-style: normal;
    font-weight: 700;
    line-height: 130%;
    /* 59.8px */
}

.arrows-btn {
    display: flex;
    gap: 20px;
    padding-top: -15px;
}

.company-name { 
    display: flex;
    align-items: center;
    gap: 380px;
}

.partners-worker {
    width: 495px;
    height: 550px;
    padding-bottom: -75px;
    border-radius: 4px;
    background: url(../../assets/images/workers.jpg) lightgray 50% / cover no-repeat;
}

.client-saying {
    display: flex;
    gap: 135px;
    padding-top: 152px;
}

.edwards-p2 {
    color: var(--gray-700, #787A80);
    padding-top: -24px;
    /* small/regular */
    font-family: Ubuntu;
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    /* 21px */
}

.edwards>h3 {
    color: var(--gray-900, #1E212C);
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    font-size: 16px;
    font-style: normal;
    font-weight: 700;
    line-height: 160%;
    /* 25.6px */
}

.edwards-p1 {
    width: 600px;
    color: var(--gray-800, #424551);

    /* base/regular */
    font-family: Arial, Helvetica, sans-serif;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 160%;
}

.edwards>img {
    padding-top: 60px;
}

.edwards {
    display: flex;
    flex-direction: column;
    align-items: start;
    gap: 24px;
}

.InDepth {
    display: flex;
    justify-content: space-between;
    padding: 20px;
    padding-top: 50px;
    gap: 20px;
}

.partners-h2 {
    display: flex;
    justify-content: center;
    padding-top: 80px;
}

.main-partners {
    background: var(--gray-200, #F4F5F6);
    height: 934px;

}
</style>