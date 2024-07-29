<template>
    <nav>
        <div>
            <div class="nav-main container">
                <div class="header-logo">
                    <img src="../../assets//icons//logo.svg" alt="CreateX">
                </div>
                <div class="header-list">
                    <ul class="nav-ul">
                        <li class="bg-red">About Us</li>
                        <li>Services</li>
                        <li>Work</li>
                        <li>News</li>
                        <li>Contacts</li>

                    </ul>
                </div>
              <div class="main-phone-chat">
                <div class="phone-chat">
                    <span> <img src="../../assets/icons/iPhone.svg" alt="Iphone"></span>
                    <span>
                        <p>Call us</p>
                        <p>(405) 555-0128</p>
                    </span>
                </div>
                <div class="phone-chat">
                    <span> <img src="../../assets/icons/chat.svg" alt="chat"></span>
                    <span>
                        <p>Talk to us</p>
                        <p>hello@createx.com</p>
                    </span>
                </div>
              </div>
            </div>
        </div>
    </nav>
</template>
<script>
export default {
    name: "Header"
};
</script>
<style scoped>
.main-phone-chat{
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 36px;
 
}
.nav-main {
    display: flex;
    justify-content: space-between;
    padding: 15px;
    align-items: center;
}

li {
    list-style-type: none;
    color: rgb(0, 0, 0);
    font-size: 18px;
    transition: color 0.3s ease;
    cursor: pointer;
}


.nav-ul {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 40px;

}

.phone-chat {
    display: flex;
    align-items: center;

}
</style>