<template >
    <section class="section login container">
        <div class="form-box">
            <div class="button-box">
                <div id="btnn" v-bind:style='{"left":(isRegister ? "110px":"0" )}'></div>
                <button type="button" class="togglebtn" @click="RegisterAndLogin()">Login</button>
                <button type="button" class="togglebtn" @click="RegisterAndLogin()">Register</button>
            </div>
            <div class="social-icons">
                <box-icon name='facebook-circle' type='logo' class="cgn" ></box-icon>
                <box-icon name='twitter' type='logo' class="cgn"></box-icon>
                <box-icon name='google' type='logo' class="cgn" ></box-icon>
            </div>
            <form id="loginn" v-bind:style='{"left":(isRegister ? "-400px":"50px" )}' class="input-group">
                <input type="text" class="input-field" placeholder="User Id" required>
                <input type="text" class="input-field" placeholder="Enter Password" required>
                <input type="checkbox" class="check-box">
                <span> Remember Me</span>
                <button type="submit" class="submit-btn">Log In</button>
            </form>
            <form id="registern" v-bind:style='{"left":(isRegister ? "50px":"450px" )}' class="input-group">
                <input type="text" class="input-field" placeholder="User Id" required>
                <input type="email" class="input-field" placeholder="Email" required>
                <input type="text" class="input-field" placeholder="Enter Password" required>
                <input type="checkbox" class="check-box">
                <span>I agree to the terms & conditions</span>
                <button type="submit" class="submit-btn">Register</button>
            </form>
        </div>
    </section>
</template>
<script>
export default {
    name: 'LoginVue',
    data() {
        return {
            isRegister: false
        }
    },
    methods: {
        RegisterAndLogin(){
            this.isRegister = ! this.isRegister
        }
    },
}
</script>
<style lang="scss" scoped>
    .login{
        overflow: hidden;
    }
    .form-box{
        width: 380px;
        height: 480px;
        position: relative;
        background: antiquewhite;
        margin: 2% auto;
        padding: 5px;
        overflow: hidden;
    }
    .button-box{
        width: 220px;
        margin: 35px auto;
        position: relative;
        box-shadow: 0 0 20px 9px #ff61241f;
        border-radius: 30px;
    }
    .togglebtn{
        padding: 10px 30px;
        cursor: pointer;
        background: transparent;
        border: 0;
        outline: none;
        position: relative;
    }
    #btnn{
        top: 0;
        left: 0;
        position: absolute;
        width: 110px;
        height: 100%;
        background: linear-gradient(to right, var(--first-color), var(--first-color-lighten));
        border-radius: 30px;
        transition: 0.5s;
    }
    .social-icons{
        margin: 30px auto;
        text-align: center;
        align-items: center;
    }
    .cgn{
        width: 30px;
        margin: 0 12px;
        box-shadow: 0 0 20px 0 #7f7f7f3d;
        cursor: pointer;
        border-radius: 50%;
    }
    .input-group{
        top: 180px;
        position: absolute;
        width: 280px;
        transition: 0.5s;
    }
    .input-field{
        width: 100%;
        padding: 10px 0;
        margin: 5px 0;
        border-top: 0;
        border-left: 0;
        border-right: 0;
        border-bottom: 1px solid #999;
        outline: none;
        background: transparent;
    }
    .submit-btn{
        width: 85%;
        padding: 10px 30px;
        cursor: pointer;
        display: block;
        margin: auto;
        background: linear-gradient(to right, var(--first-color), var(--first-color-lighten));
        border: 0;
        outline: 0;
        border-radius: 30px;
    }
    .check-box{
        margin: 30px 10px 30px 0;
    }
    span{
        color: #777;
        font-size: 12px;
        bottom: 62px;
        position: absolute;
    }
    #loginn{
        left: 50px;
    }
    #registern{
        left: 450px;
    }
</style>