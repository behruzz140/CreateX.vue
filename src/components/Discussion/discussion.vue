<template>
    <div class="discussion-bg">
        <div class="container">
            <div class="container discussion-details">
                <h3>A quick way to discuss details</h3>
                <label class="input-container">
                    Name* 
                    <input 
                        type="text" 
                        v-model="name" 
                        placeholder="Your name"
                        :class="{'input-error': !isNameValid && nameTouched}" 
                        @blur="nameTouched = true"
                        required
                    >
                    <span v-if="!isNameValid && nameTouched" class="error-message">Name is required.</span>
                </label>
                <label class="input-container">
                    Phone* 
                    <input 
                        type="tel" 
                        v-model="phone" 
                        v-mask="'(+998) ###-##-##'" 
                        placeholder="(+998) 000-00-00" 
                        :class="{'input-error': !isPhoneValid && phoneTouched}" 
                        @blur="phoneTouched = true"
                        required
                    >
                    <span v-if="!isPhoneValid && phoneTouched" class="error-message">Enter a valid phone number.</span>
                </label>
                <label class="input-container">
                    Email* 
                    <input 
                        type="email" 
                        v-model="email" 
                        placeholder="Your working email" 
                        :class="{'input-error': !isEmailValid && emailTouched}" 
                        @blur="emailTouched = true"
                        required
                    >
                    <span v-if="!isEmailValid && emailTouched" class="error-message">Enter a valid email address.</span>
                </label>
                <label class="message-label">
                    Message* 
                    <textarea 
                        class="message-input" 
                        v-model="message" 
                        placeholder="Your message" 
                        :class="{'input-error': !isMessageValid && messageTouched}" 
                        @blur="messageTouched = true"
                        @keypress.enter.prevent="handleSubmit"
                        required
                    ></textarea>
                    <span v-if="!isMessageValid && messageTouched" class="error-message">Message is required.</span>
                </label>
                <div style="display: flex; align-items: center; gap: 12px;">
                    <input 
                        ref="checkbox" 
                        class="checkbox-input" 
                        type="checkbox" 
                        v-model="checkboxChecked"
                        required
                    >
                    <span style="display: flex; flex-direction: column;">
                        <p 
                            class="checkbox-p" 
                            @click="toggleCheckbox"
                        >
                            I agree to receive communications from Createx Construction Bureau.
                        </p>
                        <span v-if="!checkboxChecked && checkboxTouched" class="error-message">You must agree to receive communications.</span>
                    </span> 
                </div>
                <button 
                    class="discussion-btn" 
                    @click="handleSubmit"
                >
                    Send Request
                </button>
            </div>
        </div>
    </div>
</template>

<script>
import { parsePhoneNumberFromString } from 'libphonenumber-js';
import VueMask from 'v-mask';

export default {
    name: 'Discussion',
    directives: { mask: VueMask.VueMaskDirective },
    data() {
        return {
            name: '',
            phone: '',
            email: '',
            message: '',
            checkboxChecked: false,
            nameTouched: false,
            phoneTouched: false,
            emailTouched: false,
            messageTouched: false,
            checkboxTouched: false
        };
    },
    computed: {
        isNameValid() {
            return this.name.trim().length > 0;
        },
        isPhoneValid() {
            const phoneNumber = parsePhoneNumberFromString(this.phone);
            return phoneNumber && phoneNumber.isValid();
        },
        isEmailValid() {
            const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return emailPattern.test(this.email);
        },
        isMessageValid() {
            return this.message.trim().length > 0;
        }
    },
    methods: {
        toggleCheckbox() {
            this.checkboxChecked = !this.checkboxChecked;
        },
        handleSubmit() {
            this.nameTouched = true;
            this.phoneTouched = true;
            this.emailTouched = true;
            this.messageTouched = true;
            this.checkboxTouched = true;

            if (this.isNameValid && this.isPhoneValid && this.isEmailValid && this.isMessageValid && this.checkboxChecked) {
                alert('Request sent successfully!');
            } else {
                if (!this.checkboxChecked) {
                    alert('You must agree to receive communications.');
                } else {
                    alert('Please fill out all required fields correctly.');
                }
            }
        }
    }
}
</script>

<style scoped>
.input-container, .message-label {
    position: relative; /* Ensure the label container is positioned relatively */
}

.input-error {
    border-color: red;
    background: rgba(255, 0, 0, 0.1);
}

.error-message {
    color: red;
    font-size: 14px;
    padding-top: 4px;
    position: absolute; /* Position the error message absolutely */
    left: 0;
    bottom: -24px; /* Adjust this value to position the error message below the input or textarea */
}

.checkbox-p {
    cursor: pointer;
}

.checkbox-input {
    accent-color: #FF5A30;
    margin-top: -22px;
}

.discussion-btn {
    display: flex;
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
    letter-spacing: 0.5px;
    text-transform: uppercase;
}

.checkbox-input {
    width: 16px;
    height: 16px;
    flex-shrink: 0;
}

.message-input {
    display: flex;
    width: 415px !important;
    height: 70px;
    padding: 11px 16px;
    align-items: center;
    border-radius: 4px;
    border: 1px solid var(--gray-400, #D7DADD);
    background: var(--gray-200, #F4F5F6);
    resize: vertical;
}

label {
    display: flex;
    flex-direction: column;
    gap: 8px;
    color: var(--gray-800, #424551);
    font-family: Ubuntu;
    font-size: 17px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
}

input {
    display: flex;
    width: 415px;
    padding: 11px 31px 12px 16px;
    align-items: center;
    border-radius: 4px;
    border: 1px solid var(--gray-400, #D7DADD);
    background: var(--gray-200, #F4F5F6);
}

.discussion-details>h3 {
    width: 415px;
    color: var(--gray-900, #1E212C);
    text-align: center;
    font-family: Ubuntu;
    font-size: 28px;
    font-style: normal;
    font-weight: 700;
    line-height: 150%;
}

.discussion-details {
    position: relative;
    top: 90px;
    left: 20%;
    display: flex;
    width: 495px;
    padding: 48px 40px;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 20px;
    border-radius: 4px;
    border: 1px solid var(--gray-300, #E5E8ED);
    background: var(--white, #FFF);
    box-shadow: 0px 60px 80px -20px rgba(30, 33, 44, 0.16), 0px 26px 24px -10px rgba(30, 33, 44, 0.10), 0px 12px 10px -6px rgba(30, 33, 44, 0.08), 0px 4px 4px -4px rgba(30, 33, 44, 0.05);
}

.discussion-bg {
    height: 826px;
    background: url(../../assets/images/discussion.jpg) lightgray 50% / cover no-repeat;
}
</style>
