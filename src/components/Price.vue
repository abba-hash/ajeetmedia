<template >
    <section class="pricing section">
        <div class="container">
            <div class="prici">
                <h1 class="section-title-center">Our Pricing</h1>
                <div class="toggle">
                    <label for="">Annually</label>
                    <div class="toggle-btn">
                        <input type="checkbox" class="checkbox" id="checkbox">
                        <label for="checkbox" class="sub" id="suv">
                            <div class="circle"></div>
                        </label>
                    </div>
                    <label for="">Monthly</label>
                </div>
            </div>
            <div class="cards">
                <div class="card shadow">
                    <ul>
                        <li class="pack">Basic</li>
                        <li class="price bottom-bar" id="basic">
                            &dollar; 199.99
                        </li>
                        <li class="bottm-bar">5600 GB Storage</li>
                        <li class="bottom-bar">2 Users Allowed</li>
                        <li class="bottom-bar">Send up to 3 GB</li>
                        <li>
                            <button class="button">Learn More</button>
                        </li>
                    </ul>
                </div>
                <div class="card active">
                     <ul>
                        <li class="pack">Professional</li>
                        <li class="price bottom-bar" id="basic">
                            &dollar; 349.99
                        </li>
                        <li class="bottm-bar">1TB Storage</li>
                        <li class="bottom-bar">30 Users Allowed</li>
                        <li class="bottom-bar">Send up to 90 GB</li>
                        <li>
                            <button class="button active-btn">Learn More</button>
                        </li>
                    </ul>
                </div>
                <div class="card shadow">
                    <ul>
                        <li class="pack">Master</li>
                        <li class="price bottom-bar" id="basic">
                            &dollar; 199.99
                        </li>
                        <li class="bottm-bar">5600 GB Storage</li>
                        <li class="bottom-bar">2 Users Allowed</li>
                        <li class="bottom-bar">Send up to 3 GB</li>
                        <li>
                            <button class="button">Learn More</button>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>
</template>
<script>
export default {
    name: 'PriceVue'
}
</script>
<style lang="scss" scoped>
    .pricing{
        background-color: antiquewhite;
    }
    .prici{
        color: hsl(233, 13%, 49%);
        margin: 3.3rem 0;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        label{
            font-size: var(--normal-font-size);
            color: var(--text-color);
        }
    }
    .toggle{
        margin-top: 2rem;
        color: hsl(234, 14%, 74%);
        display: flex;
        align-items: center;
    }
    .toggle-btn{
        margin: 0 1rem;
    }
    .checkbox{
        display: none;
    }
    .sub{
        background: var(--first-color);
        display: flex;
        justify-content: flex-start;
        align-items: center;
        height: 1.6rem;
        width: 3.3rem;
        border-radius: 1.6rem;
        padding: 0.3rem;
    }
    .circle{
        background-color: #fff;
        height: 1.4rem;
        width: 1.4rem;
        border-radius: 50%;
    }
    .checkbox:checked + .sub{
        justify-content: flex-end;
    }

    .cards{
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        margin-bottom: 3rem;
    }
    .card{
        color: hsl(233, 13%, 49%);
        background-color: #fff;
        border-radius: 0.8rem;
    }
    .active{
        background: var(--first-color);
        color: #fff;
        display: flex;
        align-items: center;
        transform: scale(1.1);
        z-index: var(--z-tooltip);
        .price{
            color: var(--container-color);
        }
        .bottom-bar{
            border-bottom: 2px solid hsla(240, 8%, 85%, 0.283);
        }
    }
    ul{
        margin: 2.6rem;
        display: flex;
        justify-content: center;
        flex-direction: column;
        align-items: center;
        li{
            display: flex;
            justify-content: center;
            width: 100%;
            padding: 1rem 0;
        }
    }
    .price{
        font-size: var(--biggest-font-size);
        color: hsl(232, 13%, 33%);
    }
    .shadow{
        box-shadow: -5px 5px 15px 1px rgba(0, 0, 0, 0.1);
    }
    .active-btn{
        background: var(--container-color);
        color: var(--first-color);
    }
    .bottom-bar{
        border-bottom: 2px solid hsla(240, 8%, 85%, 0.583);
    }
    .pack{
        font-size: 1.1rem;
    }

</style>