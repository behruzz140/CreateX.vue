<template>
    <div class="footer">
        <div class="container">
            <div style="display: flex; align-items: center; gap: 242px;">
                <div>
                    <div class="footer-icol">
                        <span><img src="../../assets/icons/logo-footer.svg" alt="logo"></span>
                        <div class="social-buttons">
                            <img class="footer-icon" src="../../assets/icons/whatsapp.svg" alt="WhatsApp">
                            <img class="footer-icon" src="../../assets/icons/messenger.svg" alt="Messenger">
                            <img class="footer-icon" src="../../assets/icons/facebook.svg" alt="Facebook">
                            <img class="footer-icon" src="../../assets/icons/twitter.svg" alt="Twitter">
                            <img class="footer-icon" src="../../assets/icons/youtube.svg" alt="YouTube">
                        </div>
                    </div>
                    <p class="footer-p">Createx Construction Bureau has been successfully operating in the USA
                        construction market since 2000. We are proud to offer you quality construction and exemplary service. Our mission is to set the highest standards for construction sphere.</p>
                </div>
                <div class="second-section">
                    <h4>Let’s stay in touch</h4>
                    <form @submit.prevent="subscribe" class="subscription-form">
                        <span class="input-btn-span">
                            <input
                                type="email"
                                class="footer-input"
                                placeholder="Your email address"
                                v-model="email"
                                :class="{ 'input-error': !isEmailValid && emailTouched }"
                                @blur="emailTouched = true"
                            />
                            <button type="submit" class="footer-btn">subscribe</button>
                        </span>
                        <p class="footer-p">*Subscribe to our newsletter to receive communications and early updates from Createx Construction Bureau.</p>
                        <p v-if="!isEmailValid && emailTouched" class="error-message">Please enter a valid email address.</p>
                    </form>
                </div>
            </div>
            <div style="display: flex; gap: 145px;">
                <span>
                    <h6 style="padding-top: 70px;">HEAD OFFICE</h6>
                    <span style="display: flex; align-items: center; gap: 4px; padding-top: 13px;">
                        <h5>Address:</h5>
                        <a class="footer-link" href="https://maps.google.com/?q=8502+Preston+Rd,+Inglewood,+New+York" target="_blank" rel="noopener noreferrer">8502 Preston Rd. Inglewood, New York</a>
                    </span>
                    <span style="display: flex; align-items: center; gap: 4px; padding-top: 13px;">
                        <h5>Call:</h5>
                        <a class="footer-link" href="tel:+14055550128">(405) 555-0128</a>
                    </span>
                    <span style="display: flex; align-items: center; gap: 4px; padding-top: 13px;">
                        <h5>Email:</h5>
                        <a class="footer-link" href="mailto:hello@createx.com">hello@createx.com</a>
                    </span>
                </span>
                <span>
                    <h6 style="padding-top: 70px;">WHO WE ARE</h6>
                    <span style="display: flex; align-items: center; gap: 4px; padding-top: 13px;">
                        <a class="footer-link" href="#">About Us</a>
                    </span>
                    <span style="display: flex; align-items: center; gap: 4px; padding-top: 13px;">
                        <a class="footer-link" href="#">Available Positions</a>
                    </span>
                    <span style="display: flex; align-items: center; gap: 4px; padding-top: 13px;">
                        <a class="footer-link" href="#">Contacts</a>
                    </span>
                </span>
                <span>
                    <h6 style="padding-top: 70px;">OUR EXPERIENCE</h6>
                    <span style="display: flex; align-items: center; gap: 4px; padding-top: 13px;">
                        <a class="footer-link" href="#">Services</a>
                    </span>
                    <span style="display: flex; align-items: center; gap: 4px; padding-top: 13px;">
                        <a class="footer-link" href="#">Work</a>
                    </span>
                    <span style="display: flex; align-items: center; gap: 4px; padding-top: 13px;">
                        <a class="footer-link" href="#">News</a>
                    </span>
                </span>
            </div>
            <span class="eng-oxiri">
                <h5 style="display: flex; align-items: center; gap: 4px;">© All rights reserved. Made with <span><img src="../../assets/icons/heart.svg" alt="heart"></span>by Createx Studio</h5>
                <span class="go-to-top">
                    <h5>GO TO TOP</h5>
                    <button @click="scrollToTop"><img src="../../assets/icons/top.svg" alt="top"></button>
                </span>
            </span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Footer',
    data() {
        return {
            email: '',
            emailTouched: false,
        };
    },
    computed: {
        isEmailValid() {
            // Simple email validation regex
            const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return emailPattern.test(this.email);
        }
    },
    methods: {
        scrollToTop() {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        },
        subscribe() {
            this.emailTouched = true;
            if (this.isEmailValid) {
                // Handle the subscription logic here (e.g., send email to server)
                alert('Thank you for subscribing!');
            } else {
                alert('Please enter a valid email address.');
            }
        }
    }
}
</script>

<style scoped>
.eng-oxiri {
    display: flex;
    justify-content: space-between;
    padding-top: 60px;
}

.go-to-top {
    display: flex;
    align-items: center;
    gap: 16px;
}

.go-to-top > button {
    width: 40px;
    height: 40px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 4px;
    background: var(--primary, #FF5A30);
}

.footer-p1 {
    color: var(--white, #FFF);
    font-family: Ubuntu;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 160%;
    opacity: 0.6;
}

h6 {
    color: var(--white, #FFF);
    font-family: Ubuntu;
    font-size: 16px;
    font-style: normal;
    font-weight: 700;
    line-height: 150%;
    letter-spacing: 1px;
    text-transform: uppercase;
    cursor: pointer;
}

.input-btn-span {
    display: flex;
    align-items: center;
    padding-top: 24px;
}

h5 {
    color: var(--white, #FFF);
    font-family: Ubuntu;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 160%;
}

.footer-btn {
    display: flex;
    width: 131px;
    padding: 0px 32px;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    border-left: none !important;
    padding-left: -2px;
    border-radius: 0px 4px 4px 0px;
    background: var(--primary, #FF5A30);
    color: var(--white, #FFF);
    text-align: center;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    font-size: 14px;
    font-style: normal;
    font-weight: 700;
    line-height: 44px;
    letter-spacing: 0.5px;
    text-transform: uppercase;
}

.second-section {
    width: 495px;
    color: var(--white, #FFF);
    font-family: Ubuntu;
    font-size: 24px;
    font-style: normal;
    font-weight: 700;
    line-height: 150%;
}

.footer-input {
    display: flex;
    height: 42px;
    padding: 11px 59px 12px 16px;
    font-size: 16px;
    align-items: center;
    flex-shrink: 0;
    border-right: none !important;
    border-radius: 4px;
    border: 1px solid rgba(255, 255, 255, 0.20);
    background: rgba(255, 255, 255, 0.12);
    color: rgba(255, 255, 255, 0.558);
}

.footer-input.input-error {
    border-color: red;
    background: rgba(255, 0, 0, 0.1);
}

.footer-p {
    width: 483px;
    color: var(--white, #FFF);
    padding-top: 24px;
    font-family: sans-serif;
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    opacity: 0.6;
    cursor: pointer;
}

.footer-icol {
    display: flex;
    align-items: center;
    gap: 60px;
}

.footer {
    height: 566px;
    flex-shrink: 0;
    background: var(--gray-900, #1E212C);
    padding-top: 80px;
}

.social-buttons {
    display: flex;
    align-items: center;
    gap: 20px;
}

.footer-icon {
    width: 30px;
    height: 30px;
    padding: 5px;
    cursor: pointer;
    transition: transform 0.2s ease;
    position: relative;
}

.footer-icon:hover {
    transform: scale(1.2);
    border-radius: 50%;
}

.footer-icon[alt="WhatsApp"]:hover {
    background: #25d366;
}

.footer-icon[alt="Messenger"]:hover {
    background: #00b2ff;
}

.footer-icon[alt="Facebook"]:hover {
    background: #3b5998;
}

.footer-icon[alt="Twitter"]:hover {
    background: #1da1f2;
}

.footer-icon[alt="YouTube"]:hover {
    background: #ff0000;
}

.error-message {
    color: red;
    font-size: 14px;
    padding-top: 8px;
}

/* Additional styles for links */
.footer-link {
    color: var(--white, #FFF);
    font-family: Ubuntu;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 160%;
    text-decoration: none;
}

.footer-link:hover {
    text-decoration: underline;
}
</style>
