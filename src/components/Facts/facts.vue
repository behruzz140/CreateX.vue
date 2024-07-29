<template>
    <div class="container facts-main">
        <div>
            <h2 class="title">Some facts and figures</h2>
        </div>
        <div class="statistics container">
            <div v-for="stat in stats" :key="stat.id" class="stat-item">
                <div class="circle" :style="{
                    borderColor: stat.color,
                    '--mask-transform': stat.value <= 100 ? 'rotate(' + (stat.value / 100 * 180) + 'deg)' : 'none',
                    '--fill-transform': stat.value <= 100 ? 'rotate(' + (stat.value / 100 * 180) + 'deg)' : 'none',
                    '--background-color': stat.value <= 100 ? 'none' : '#e6e6e6'
                }">
                    <div class="mask full" :style="{ transform: 'var(--mask-transform)' }"></div>
                    <div class="mask half">
                        <div class="fill" :style="{ transform: 'var(--fill-transform)', backgroundColor: stat.color }">
                        </div>
                    </div>
                    <div class="inside-circle">
                        <p>{{ stat.value }}</p>
                    </div>
                </div>
                <h2>{{ stat.title }}</h2>
            </div>
        </div>

        <div>
            <h2 class="facts-h2">Recent news</h2>
        </div>

        <div class="recent-news">

            <div class="facts-card-main">
                <img src="../../assets/images/SolarMan.jpg" alt="solar">
                <div class="padding-berish-kk" style="display: flex; flex-direction: column; align-items: start;">
                    <span>
                        <h3 class="hover-h3">How to Build Climate Change-Resilient Infrastructure</h3>
                    </span>
                    <span class="solar-textP" style="display: flex; align-items: center; gap: 8px; padding-top: 12px;">
                        <p>Industry News</p>
                        <span style="width: 1px;
height: 12px;background: #787A80;"></span>
                        <p>June 24, 2020</p>
                        <span style="width: 1px;
height: 12px;background: #787A80;"></span>
                        <img src="../../assets//icons/chat2.svg" alt="">
                        <p>4 comments</p>
                    </span>
                    <p class="venenatis">Ipsum aliquet nisi, hendrerit rhoncus quam tortor, maecenas faucibus.
                        Tincidunt aliquet sit vel,
                        venenatis nulla. Integer bibendum turpis convallis enim, nibh convallis...</p>
                </div>
            </div>



            <div class="gap-in-2-img">
                <div class="cards-2-main">
                    <img src="../../assets/images/kaska.jpg" alt="solar">

                    <div class="padding-berish-kk" style="display: flex; flex-direction: column; align-items: start;">
                        <span>
                            <h3 class="hover-h3">How Construction Can Help Itself</h3>
                        </span>
                        <span class="solar-textP"
                            style="display: flex; align-items: center; gap: 8px; padding-top: 12px;">
                            <p>Innovation</p>
                            <span style="width: 1px;
height: 12px;background: #787A80;"></span>
                            <p>June 12, 2020</p>
                            <span style="width: 1px;
height: 12px;background: #787A80;"></span>
                            <img src="../../assets//icons/chat2.svg" alt="">
                            <p>No comments</p>
                        </span>

                    </div>
                </div>


                <div class="cards-2-main">
                    <img src="../../assets/images/kaska2.jpg" alt="solar">
                    <div class="padding-berish-kk" style="display: flex; flex-direction: column; align-items: start;">
                        <span>
                            <h3 class="hover-h3">Types of Flooring Materials</h3>
                        </span>
                        <span class="solar-textP"
                            style="display: flex; align-items: center; gap: 8px; padding-top: 12px;">
                            <p>Company News</p>
                            <span style="width: 1px;
height: 12px;background: #787A80;"></span>
                            <p>December 1, 2019</p>
                            <span style="width: 1px;
height: 12px;background: #787A80;"></span>
                            <img src="../../assets//icons/chat2.svg" alt="">
                            <p>No comments</p>
                        </span>

                    </div>
                </div>
            </div>


        </div>
        <div class="service-footer">
            <h2>Explore all our news posts</h2>
            <button class="service-btn">View all news</button>
        </div>

    </div>
</template>



<script>
export default {
    name: "Facts",
    data() {
        return {
            stats: [
                { id: 1, title: "Totally satisfied clients", value: 98, color: '#f4a615' },
                { id: 2, title: "Years of experience", value: 20, color: '#e91e63' },
                { id: 3, title: "Working hours spent", value: 9452, color: '#3f51b5' },
                { id: 4, title: "Succeeded projects", value: 100, color: '#4caf50' }
            ]
        };
    }
};
</script>
<style scoped>
.service-footer{
    padding: 0 0 85px 0;
}
.gap-in-2-img{
    display: flex; 
    flex-direction: column;
    gap: 30px;
    padding-left: 30px;
}
.facts-h2 {
text-align: center;
    color: var(--gray-900, #1E212C);


    /* h1 */
    font-family: Ubuntu;
    font-size: 46px;
    font-style: normal;
    font-weight: 700;
    line-height: 130%;
    /* 59.8px */
}

.hover-h3 {
    padding-top: 20px;
}

.hover-h3:hover {
    transition: all 0.2s;
    color: var(--primary, #FF5A30);
    cursor: pointer;
}

.padding-berish-kk {
    padding-left: 16px;
}

.recent-news {
    padding-bottom: 85px;
    display: flex;
    justify-content: space-between;
    padding-top: 60px;
}

.cards-2-main {
    
    width: 495px;
    height: 255px;
    flex-shrink: 0;
    border-radius: 4px;
    background: var(--main-white, #FFF);

    /* shadow/regular */
    box-shadow: 0px 80px 80px -20px rgba(154, 156, 165, 0.16), 0px 30px 24px -10px rgba(154, 156, 165, 0.10), 0px 12px 10px -6px rgba(154, 156, 165, 0.08), 0px 4px 4px -4px rgba(30, 33, 44, 0.05);
}

.facts-card-main {
    border-radius: 4px;
    background: var(--white, #FFF);

    box-shadow: 0px 80px 80px -20px rgba(154, 156, 165, 0.08), 0px 30px 24px -10px rgba(154, 156, 165, 0.05), 0px 12px 10px -6px rgba(154, 156, 165, 0.04), 0px 4px 4px -4px rgba(30, 33, 44, 0.03);
}

.venenatis {
    width: 657px;
    text-align: start;
    padding: 24px 0;
    color: var(--gray-800, #424551);
    font-family: Ubuntu;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 160%;
    /* 25.6px */
}

.solar-textP {
    color: var(--gray-700, #787A80);

    /* small/regular */
    font-family: Ubuntu;
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    /* 21px */
}


.title {
    display: flex;
    justify-content: center;
    padding-top: 180px;
    font-size: 2em;
    font-weight: bold;
}

.statistics {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 60px 20px;
    max-width: 800px;
}

.stat-item {
    text-align: center;
    padding: 0 15px;
    padding: 20px;
}

.circle {
    position: relative;
    width: 120px;
    height: 120px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    border: 5px solid var(--border-color, #ddd);
}


.circle .mask {
    clip: rect(0px, 120px, 120px, 60px);
}

.circle .mask .fill {
    clip: rect(0px, 60px, 120px, 0px);
}

.circle .inside-circle {
    width: 90px;
    height: 90px;
    border-radius: 50%;
    background: #ffffff;
    line-height: 90px;
    text-align: center;
    z-index: 100;
    font-weight: bold;
    font-size: 1.2em;
}

.stat-item h2 {
    padding-top: 20px;
    color: var(--gray-900, #1E212C);
    text-align: center;
    font-family: Ubuntu;
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;

}

.stat-number {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 120px;
    height: 120px;
    background: #e6e6e6;
    border-radius: 50%;
    font-size: 1.5em;
    color: #333;
}
</style>
