<template >
    <section class="newsletter section container">
        <div class="newsletter-bg grid">
            <div>
                <h2 class="newsletter-title">Subscribe Our <br> Newsletter</h2>
                <p class="newsletter-description">
                    Don't miss out on your discounts. Subscribe to our email 
                    newsletter to get the best offers, discounts, coupons, 
                    gifts and much more.
                </p>
            </div>
            <form class="newsletter-subscribe">
                <input type="email" placeholder="Enter your email" class="newsletter-input">
                <button class="newsletter-button">
                   SUBSCRIBE
                </button>
            </form>  
        </div>
    </section>
</template>
<script>
export default {
    name: 'SubscribeVue'
}
</script>
<style lang="scss" scoped>
    .newsletter-bg{
        background-color: var(--first-color);
        padding: 3rem 1.5rem;
        text-align: center;
        row-gap: 2.5rem;
        @media screen and (min-width: 767px){
            grid-template-columns: repeat(2, 1fr);
            align-items: center;
            text-align: initial;
            column-gap: 2rem;
            padding: 4.5rem;
        }
    }
    .newsletter-title{
        font-size: var(--h2-font-size);
        color: hsl(0, 0%, 15%);
        margin-bottom: var(--mb-1-5);
    }
    .newsletter-description{
        color: hsl(0, 0%, 35%);
    }
    .newsletter-subscribe{
        display: flex;
        flex-direction: column;
        row-gap: .75rem;
        @media screen and (min-width: 767px){
            flex-direction: row;
        }
    }
    .newsletter-input{
        border: none;
        outline: none;
        background-color: hsl(0, 0%, 94%);
        padding: 1.25rem 1rem;
        color: hsl(0, 0%, 15%);
        @media screen and (min-width: 767px){
            width: 100%;
        }
    }
    .newsletter-button{
        display: inline-block;
        background-color: var(--first-color);
        color: #1A1A1A;
        padding: 1.25rem 2rem;
        font-weight: var(--font-semi-bold);
        transition: .3s;

        &:hover{
          background-color: var(--first-color-alt);
        }
    }
</style>