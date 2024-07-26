<template>
<div>
       <!-- input start -->
       <div class="const-input" style="margin-left: 120px;" >
                <div>
                    <h1>Want to know more? Ask us a question:</h1>
                </div>
                <div style="display: flex; gap: 24px; padding: 48px 60px;">
                    <div class="label-int">
                        <label class="const-label">
                            <h3 style="">Name</h3>
                            <input class="name-input" type="text" placeholder="Your name">
                        </label>
                    </div>

                    <div class="label-int">
                        <label class="const-label">
                            <h3 style="">Phone</h3>
                            <input class="name-input" type="text" placeholder="Your phone">
                        </label>
                    </div>

                    <div class="label-int message">
                        <label class="const-label">
                            <h3 style="">Message</h3>
                            <input class="name-input message" type="text" placeholder="Your message">
                        </label>
                    </div>
                    <button class="send-btn"> Send</button>
                </div>
            </div>
            <!-- input end -->
    <div class="servicePage container">
        
            
      
        <div>
       
            <div class="const-part2">
                <span style="display: flex;
           flex-direction: column; align-items: center; padding-top: 60px;">
                    <h1>Our core values</h1>
                    <p>Our mission is to set the highest standards for construction sphere.</p>
                </span>
            </div>
        </div>
        <!-- cards  start-->
        <div class="main-card">
            <div class="service-card">
                <span class="card-detail">
                    <img src="../../assets/icons/ic.svg" alt="ic">
                    <h1>Development </h1>
                </span>
            </div>

            <div class="service-card">
                <span class="card-detail">
                    <img src="../../assets/icons/ic-development.svg" alt="ic">
                    <h1>Development </h1>
                </span>
            </div>


            <div class="service-card">
                <span class="card-detail">
                    <img src="../../assets/icons/ic-pantone.svg" alt="ic">
                    <h1>Design </h1>
                </span>
            </div>

            <div class="service-card">
                <span class="card-detail">
                    <img src="../../assets/icons/ic-paint.svg" alt="ic">
                    <h1>Repairs </h1>
                </span>
            </div>
        </div>

        <!-- cards end -->
        <div class="service-footer">
            <h1>Learn more about our services</h1>
            <button class="service-btn">View services</button>
        </div>
    </div>
</div>
</template>
<script>
export default {
    name: 'ServicePage',
}
</script>
<style>
/* inputs */


.send-btn {
    margin-top: 33px;
    display: inline-flex;
    padding: 0px 32px;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    border-radius: 4px;
    background: var(--primary, #FF5A30);
    color: var(--white, #FFF);
    text-align: center;
    font-family: Ubuntu;
    font-size: 14px;
    font-style: normal;
    font-weight: 700;
    line-height: 44px;
    /* 314.286% */
    letter-spacing: 0.5px;
    text-transform: uppercase;

}

.name-input {
    margin-top: 8px;
    display: flex;
    width: 270px;
    padding: 10px;
    align-items: center;
    border-radius: 4px;
    border: 1px solid var(--gray-400, #D7DADD);
    background: var(--gray-200, #F4F5F6);
}


.label-int {
    display: flex;
    flex-direction: column;

}


.const-input>div>h1 {
    color: var(--gray-900, #1E212C);
    text-align: center;
    margin-top: 40px;
    /* h3 */
    font-family: Ubuntu;
    font-size: 28px;
    font-style: normal;
    font-weight: 700;
    line-height: 150%;
    /* 42px */
}

.const-input {
    /* margin-top: 340px; */
    /* margin-bottom: -190px; */
    width: 1230px;
    height: 243px;
    flex-shrink: 0;
    border-radius: 4px;
    background: var(--white, #fff);

    /* shadow/small */
    box-shadow: 0px 80px 80px -20px rgba(154, 156, 165, 0.08), 0px 30px 24px -10px rgba(154, 156, 165, 0.05), 0px 12px 10px -6px rgba(154, 156, 165, 0.04), 0px 4px 4px -4px rgba(30, 33, 44, 0.03);
}







.service-footer {
    display: flex;
    justify-content: center;
    gap: 40px;
    align-items: center;
    margin-top: 85px;
}

.service-btn {
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

.service-footer>h1 {
    color: var(--gray-900, #1E212C);

    /* h3 */
    font-family: Ubuntu;
    font-size: 28px;
    font-style: normal;
    font-weight: 700;
    line-height: 150%;
    /* 42px */
}

.main-card {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 60px;
    gap: 30px;
}

.card-detail {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 24px;
}

.card-detail>h1 {
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

.service-card {
    display: flex;
    width: 285px;
    height: 285px;
    padding: 89px 80px 90px 80px;
    justify-content: center;
    align-items: center;
    flex-shrink: 0;
    border-radius: 4px;
    border: 1px solid var(--gray-300, #E5E8ED);
    background: var(--white, #FFF);
    box-shadow: 0px 80px 80px -20px rgba(154, 156, 165, 0.08), 0px 30px 24px -10px rgba(154, 156, 165, 0.05), 0px 12px 10px -6px rgba(154, 156, 165, 0.04), 0px 4px 4px -4px rgba(30, 33, 44, 0.03);
}

.servicePage {
    /* opacity: 0.9; */
    margin-top: -180px;
    padding-bottom: 85px;
    background: url(../../assets/images/servicePage.png) lightgray 50% / cover no-repeat;
}
</style>