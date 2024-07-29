<template>
  <!-- input start -->
  <div class="servicePage">
  <div class="container ">
        <div class="const-input">
            <div>
                <h2>Want to know more? Ask us a question:</h2>
            </div>
            <div class="what-know-more" style="display: flex; gap: 24px; padding: 48px 60px;">
                <div class="label-int">
                    <label class="const-label">
                        <h3 style="">Name</h3>
                        <input class="name-input" type="text" placeholder="Your name" required>
                    </label>
                </div>

                <div class="label-int">
                    <label class="const-label">
                        <h3 style="">Phone</h3>
                        <input class="name-input" type="tel" placeholder="+998" pattern="\+998-\d{2}-\d{3}-\d{2}-\d{2}"
                            title="+998" required>
                    </label>
                </div>

                <div class="label-int">
                    <label class="const-label">
                        <h3>Message</h3>
                        <textarea class="name-input message-input" placeholder="Your message" rows="1"
                            required></textarea>

                    </label>
                    <button class="send-btn">Send</button>
                </div>

            </div>
        </div>
      </div>
        <!-- input end -->
    
      
        <div>
            <div class="const-part2">
                <span style="display: flex; flex-direction: column; align-items: center; padding-top: 60px;">
                    <h2>Our core values</h2>
                    <p>Our mission is to set the highest standards for construction sphere.</p>
                </span>
            </div>
        </div>
        <!-- cards start -->
        <div class="main-card container">
            <div class="service-card">
                <span class="card-detail">
                    <img src="../../assets/icons/ic.svg" alt="ic">
                    <h2>Interior </h2>
                </span>
            </div>

            <div class="service-card">
                <span class="card-detail">
                    <img src="../../assets/icons/ic-development.svg" alt="ic">
                    <h2>Project </h2>
                </span>
            </div>

            <div class="service-card">
                <span class="card-detail">
                    <img src="../../assets/icons/ic-pantone.svg" alt="ic">
                    <h2>Design </h2>
                </span>
            </div>

            <div class="service-card">
                <span class="card-detail">
                    <img src="../../assets/icons/ic-paint.svg" alt="ic">
                    <h2>Repairs </h2>
                </span>
            </div>
        </div>
        <!-- cards end -->
        <div class="service-footer">
            <h2>Learn more about our services</h2>
            <button class="service-btn">View services</button>
        </div>
    </div>

</template>

<script>
export default {
    name: 'ServicePage',
    methods: {
        validatePhoneNumber(event) {
            const input = event.target;
            const value = input.value;
            const regex = /^\+998-\d{2}-\d{3}-\d{2}-\d{2}$/;

            if (!regex.test(value) && value !== '') {
                input.setCustomValidity('+998-XX-XXX-XX-XX');
            } else {
                input.setCustomValidity('');
            }
        }
    }
};
</script>


<style>
/* inputs */
.const-label>h3 {
    padding-bottom: 8px;
}

.message-input {
    width: 340px !important;
}

.send-btn {
    margin-top: 32px;
    padding: 0px 32px;
    align-items: center;
    gap: 10px;
    border-radius: 4px;
    background: var(--primary, #FF5A30);
    color: #fff;

}


.name-input {
    padding-top: 8px;
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
    gap: 24px;
}

.const-input>div>h2 {
    color: var(--gray-900, #1E212C);
    text-align: center;
    padding-top: 40px;
    font-family: Ubuntu;
    font-size: 28px;
    font-style: normal;
    font-weight: 700;
    line-height: 150%;
}

.const-input {
    width: 1230px;
    height: 243px;
    flex-shrink: 0;
    border-radius: 4px;
    background: var(--white, #fff);
    box-shadow: 0px 80px 80px -20px rgba(154, 156, 165, 0.08), 0px 30px 24px -10px rgba(154, 156, 165, 0.05), 0px 12px 10px -6px rgba(154, 156, 165, 0.04), 0px 4px 4px -4px rgba(30, 33, 44, 0.03);
}

.service-footer {
    display: flex;
    justify-content: center;
    gap: 40px;
    align-items: center;
    padding-top: 85px;
}

.service-btn {
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
    background: var(--primary, #FF5A30);
}

.service-footer>h2 {
    color: var(--gray-900, #1E212C);
    font-family: Ubuntu;
    font-size: 28px;
    font-style: normal;
    font-weight: 700;
    line-height: 150%;
}

.main-card {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 60px 0 85px 0;
    gap: 30px;
}

.card-detail {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 24px;
}

.card-detail>h2 {
    color: var(--gray-900, #1E212C);
    text-align: center;
    font-family: Ubuntu;
    font-size: 20px;
    font-style: normal;
    font-weight: 700;
    line-height: 150%;
}

.service-card {
    display: flex;
    width: 285px;
    height: 285px;
    padding: 89px 80px 90px 80px;
    justify-content: center;
    align-items: center;

    border-radius: 4px;
    border: 1px solid var(--gray-300, #E5E8ED);
    background: var(--white, #FFF);
    box-shadow: 0px 80px 80px -20px rgba(154, 156, 165, 0.08), 0px 30px 24px -10px rgba(154, 156, 165, 0.05), 0px 12px 10px -6px rgba(154, 156, 165, 0.04), 0px 4px 4px -4px rgba(30, 33, 44, 0.03);
}

.servicePage {
    padding-bottom: 85px;
    /* opacity: 0.9; */
    background: url(../../assets/images/servicePage.png) lightgray 50% / cover no-repeat;
}
</style>