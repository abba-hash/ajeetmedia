<template >
    <header class="header" :class="{'scrolled-nav': scrolledNav}">
        <nav class="nav container">
            <router-link to="/" class="nav-logo">
                <span class="nav-icon">ZANFX</span>
            </router-link>
            <div :class="isOpen ? 'nav-menu show-menu' : 'nav-menu'">
                <ul class="nav-list">
                    <li class="nav-item"  v-for="menu in menus" :key="menu.id" 
                    v-on:click="menuOpen()">
                        <router-link :to= "`${menu.path}`" class="nav-link"
                        >{{menu.text}}</router-link>
                    </li>
                    <box-icon name='toggle-left' class="change-theme"></box-icon>
                </ul>
            </div>
            <div class="nav-btns">
                <div class="nav-user">
                    <router-link to="/login">
                       <box-icon name='user' v-show="mobile"></box-icon>
                    </router-link>
                </div>
                <div class="nav-toggle">
                    <box-icon name='grid-alt' v-on:click="menuOpen()" 
                     v-show="mobile"></box-icon>
                </div>
            </div>
            <router-link to="/login" class="button button-header">
                Login
            </router-link>
        </nav>
    </header>
</template>
<script>
export default {
    name: 'NavBar',
    data() {
        return {
            menus: [
                {
                    id: 1,
                    text: 'Home',
                    path: '/'
                },
                 {
                    id: 2,
                    text: 'Pricing',
                    path: '/pricing'
                },
                 {
                    id: 3,
                    text: 'Blog',
                    path: '/blog'
                },
                 {
                    id: 4,
                    text: 'Contact',
                    path: '/contact'
                },
            ],
            isOpen: false,
            windowWidth: null,
            mobile: null,
            scrolledNav: null,
        }
    },
    created() {
        window.addEventListener('resize', this.checkScreen);
        this.checkScreen();
    },
    mounted() {
        window.addEventListener('scroll',this.updateScroll);
    },
    methods: {
        menuOpen(){
            this.isOpen = !this.isOpen;
        },
        checkScreen(){
            this.windowWidth = window.innerWidth;
            if(this.windowWidth <= 767){
                this.mobile = true;
                return;
            }else{
                this.mobile = false;
                this.isOpen = false;
                return;
            }
        },
        updateScroll(){
            const scrollPosition = window.scrollY;

            if(scrollPosition > 50){
                this.scrolledNav = true;
                return;
            }else{
                this.scrolledNav = false;
            }
        },
    },
}
</script>
<style lang="scss" scoped>
    .header{
        width: 100%;
        background-color: var(--body-color);
        position: fixed;
        top: 0;
        left: 0;
        z-index: var(--z-fixed);
        transition: 0.5s;
    }
    .nav{
        position: relative;
        height: var(--header-height);
        display: flex;
        justify-content: space-between;
        align-items: center;
        @media screen and (min-width: 767px){
            height: calc(var(--header-height) + 1.5rem);
        }
    }
    .nav-logo,.nav-toggle,.nav-user{
        color: var(--title-color);
        font-size: 1.25rem;
        cursor: pointer;
    }
    .nav-icon{
        font-size: 1.25rem;
        width: 50px;
    }
    .nav-btns{
        display: flex;
        align-items: center;
        justify-content: center;
        column-gap: 1rem;
    }
    .nav-menu{
        @media screen and(max-width: 767px) {
            position: fixed;
            background-color: var(--container-color);
            box-shadow: 0 0 4px rgba(0, 0, 0, 0.1);
            padding: 2.5rem 0;
            width: 95%;
            top: -100%;
            left: 0;
            right: 0;
            margin: 0 auto;
            transition: .4s;
            border-radius: 2rem;
            z-index: var(--z-fixed);
        }
    }
    .show-menu {
        top: calc(var(--header-height) + 1rem);
    }
    .nav-list{
        display: flex;
        flex-direction: column;
        align-items: center;
        row-gap: 1.5rem;
        @media screen and (min-width: 767px){
            flex-direction: row;
            column-gap: 2rem;
        }
    }
    .nav-link{
        color: var(--title-color);
        font-weight: var(--font-semi-bold);

        &:hover{
            color: var(--first-color);
            border-radius: 50%;
        }

        &.router-link-exact-active{
            position: relative;
            color: var(--first-color);

            &::before{
                content: '';
                position: absolute;
                bottom: -.3rem;
                left: 45%;
                width: 5px;
                height: 5px;
                background-color: var(--first-color);
                border-radius: 50%;
            }
        }
    }
    .change-theme {
       position: absolute;
       right: 1.5rem;
       top: 2.2rem;
       color: var(--title-color);
       font-size: 1.8rem;
       cursor: pointer;
       @media screen and (min-width: 767px){
           position: initial;
       }
    }
    .scrolled-nav{
        box-shadow:  0 1px 4px rgba(0, 0, 0, 0.1);
    }
</style>