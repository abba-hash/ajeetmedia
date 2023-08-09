<template >
    <footer class="footer section">
        <div class="footer-container container grid">
            <div class="footer-content">
                <router-link to="/" class="footer-logo">ZANFX</router-link>
                <p class="footer-description">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Animi, eos!</p>
            </div>
            <div class="footer-content">
                <h3 class="footer-title">Our Services</h3>
                <ul class="footer-links">
                    <li><router-link to="#" class="footer-link">Pricing</router-link></li>
                    <li><router-link to="#" class="footer-link">Discounts</router-link></li>
                    <li><router-link to="#" class="footer-link">Report a bug</router-link></li>
                    <li><router-link to="#" class="footer-link">Terms of Service</router-link></li>
                </ul>
            </div>
            <div class="footer-content">
                <h3 class="footer-title">Our Company</h3>
                <ul class="footer-links">
                    <li><router-link to="#" class="footer-link">Blog</router-link></li>
                    <li><router-link to="#" class="footer-link">Our mision</router-link></li>
                    <li><router-link to="#" class="footer-link">Get in touch</router-link></li>
                </ul>
            </div>
            <div class="footer-content">
                <h3 class="footer-title">Community</h3>
                <ul class="footer-links">
                    <li><router-link to="#" class="footer-link">Support</router-link></li>
                    <li><router-link to="#" class="footer-link">Questions</router-link></li>
                    <li><router-link to="#" class="footer-link">Customer help</router-link></li>
                </ul>
            </div>
            <div class="footer-social">
                <router-link to="#" class="footer-social-link"><box-icon name='facebook-circle' type='logo' ></box-icon></router-link>
                <router-link to="#" class="footer-social-link"><box-icon name='twitter' type='logo' ></box-icon></router-link>
                <router-link to="#" class="footer-social-link"><box-icon name='instagram-alt' type='logo' ></box-icon></router-link>
                <router-link to="#" class="footer-social-link"><box-icon name='pinterest' type='logo' ></box-icon></router-link>
            </div>
        </div>
        <p class="footer-copy">&#169; ZANFX. All right reserved</p>
    </footer>
</template>
<script>
import 'boxicons'
export default {
    name: 'FooterVue',
}
</script>
<style lang="scss" scoped>
    .footer{
        background-color: var(--first-color-lighten);
        padding-bottom: 2rem;
    }
    .footer-container{
        row-gap: 2rem;
        @media screen and (min-width: 576px){
            grid-template-columns: repeat(2, 1fr);
        }
        @media screen and (min-width: 968px){
            grid-template-columns: repeat(5, 1fr);
        }
        @media screen and (min-width: 1024px){
            column-gap: 3rem;
        }
    }
    .footer-logo,.footer-title{
        font-size: var(--h3-font-size);
        margin-bottom: var(--mb-0-75);
    }
    .footer-logo{
        display: inline-block;
        font-weight: var(--font-semi-bold);
        color: var(--title-color);
    }
    .footer-description,.footer-link{
        font-size: var(--small-font-size);
    }
    .footer-links{
        display: grid;
        row-gap: .5rem;
    }
    .footer-link{
        color: var(--title-color);
    }
    .footer-social{
        display: flex;
        column-gap: 1.5rem;
        @media screen and (min-width: 968px){
            align-items: flex-start;
        }
    }
    .footer-social-link{
        font-size: 1.25rem;
        color: var(--title-color);
        @media screen and (min-width: 968px){
            font-size: 1.45rem;
        }
    }
    .footer-copy{
        margin-top: 6rem;
        text-align: center;
        font-size: var(--smaller-font-size);
        color: var(--text-color);
    }
</style>