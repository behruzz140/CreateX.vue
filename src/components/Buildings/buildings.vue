<template>
    <div class="container building-main">
        <div style="display: flex;  padding-top: 120px; justify-content: space-between;">
            <h2 class="building-h2">Browse our selected projects
                and learn more about our work</h2>
            <div style="display: flex; gap: 12px; padding-top: 66px;">
                <button class="styled-button">
                    <img src="../../assets/icons/left-arr.svg" alt="left">
                </button>
                <button class="styled-button">
                    <img src="../../assets/icons/right-arr.svg" alt="right">
                </button>
            </div>
        </div>
        <div class="building-cards">
            <div class="buildings-container">
                <img src="../../assets/images/building.jpg" alt="building">
                <span class="building-card-text">
                    <h3>Red Finger Building</h3>
                    <p>Business Centers</p>
                    <button>View Project</button>
                </span>
            </div>

            <div class="buildings-container">
                <img src="../../assets/images/building.jpg" alt="building">
                <span class="building-card-text">
                    <h3>Red Finger Building</h3>
                    <p>Business Centers</p>
                    <button>View Project</button>
                </span>
            </div>



            <div class="buildings-container">
                <img src="../../assets/images/building.jpg" alt="building">
                <span class="building-card-text">
                    <h3>Red Finger Building</h3>
                    <p>Business Centers</p>
                    <button>View Project</button>
                </span>
            </div>

        </div>
        <span class="explore-portfolio">
            <h3 class="buildings-h3">Explore all our works</h3>
            <button class="view-portfolio">View portfolio</button>
        </span>
    </div>
</template>
<script>
export default {
    name: "Buildings"
}
</script>
<style scoped>

.explore-portfolio{
    display: flex;
    align-items: center;
    justify-content: center;
    padding-top: 85px;
    gap: 40px;
}
.building-h2 {
    width: 705px;
    color: var(--gray-900, #1E212C);
    font-family: Ubuntu;
    font-size: 46px;
    font-style: normal;
    font-weight: 700;
    line-height: 130%;
    /* 59.8px */
}

.buildings-h3 {
    color: var(--gray-900, #1E212C);

    /* h3 */
    font-family: Arial, Helvetica, sans-serif;
    font-size: 28px;
    font-style: normal;
    font-weight: 700;
    line-height: 150%;
    /* 42px */
}

.building-main {
    padding-bottom: 125px;
}

.styled-button {
    border-radius: 50%;
    width: 48px;
    height: 48px;
    flex-shrink: 0;
    background: #FF5A30;
    display: flex;
    align-items: center;
    justify-content: center;
}

.view-portfolio {
    display: flex;
    padding: 0px 40px;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    border-radius: 4px;
    background: var(--primary, #FF5A30);
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
}

.building-cards {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-top: 60px;
}


.building-card-text>button {
    padding-top: 20px;
    display: inline-flex;
    padding: 0px 32px;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    border-radius: 4px;
    border: 1px solid var(--primary, #FF5A30);
    color: var(--primary, #FF5A30);
    text-align: center;
    font-family: Ubuntu;
    font-size: 14px;
    font-style: normal;
    font-weight: 700;
    line-height: 44px;
    /* 314.286% */
    letter-spacing: 0.5px;
    text-transform: uppercase;
    /* visibility: hidden; */
}

.building-card-text {
    display: flex;
    flex-direction: column;
    align-items: center;
}

.building-card-text>p {
    width: 350px;
    color: var(--gray-700, #787A80);
    text-align: center;
    font-family: Ubuntu;
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;

}

.building-card-text>h3 {
    padding-top: 16px;
    width: 350px;
    color: var(--gray-900, #1E212C);
    text-align: center;
    /* lead/bold */
    font-family: Ubuntu;
    font-size: 20px;
    font-style: normal;
    font-weight: 700;
    line-height: 150%;
    /* 30px */
}

.buildings-container {
    padding-bottom: 85px;
    display: flex;
    width: 390px;
    height: 515px;
    padding-bottom: 24px;
    flex-direction: column;
    align-items: center;
    gap: 16px;
    flex-shrink: 0;
    /* shadow/small */
    box-shadow: 0px 80px 80px -20px rgba(154, 156, 165, 0.08),
        0px 30px 24px -10px rgba(154, 156, 165, 0.05),
        0px 12px 10px -6px rgba(154, 156, 165, 0.04),
        0px 4px 4px -4px rgba(30, 33, 44, 0.03);
}
</style>