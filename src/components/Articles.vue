<template>
    <section class="article">
        <div class="container">
            <div class="article-content">
                <div class="article-item">
                    <div class="article-img">
                        <img src="../assets/image/security-ilustration.svg" alt="">
                        <span class="likes"><box-icon name='heart' color="white" ></box-icon>34</span>
                        <span class="cat-title">Politics & Par</span>
                    </div>
                    <div class="article-title">
                        <router-link to="#">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste
                        </router-link>
                    </div>
                </div>
                <div class="article-item">
                    <div class="article-img">
                        <img src="../assets/image/security-ilustration.svg" alt="">
                        <span class="likes"><box-icon name='heart' color="white" ></box-icon>34</span>
                        <span class="cat-title">Politics & Par</span>
                    </div>
                    <div class="article-title">
                        <router-link to="#">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste
                        </router-link>
                    </div>
                </div>
                <div class="article-item">
                    <div class="article-img">
                        <img src="../assets/image/security-ilustration.svg" alt="">
                        <span class="likes"><box-icon name='heart' color="white" ></box-icon>34</span>
                        <span class="cat-title">Politics & Par</span>
                    </div>
                    <div class="article-title">
                        <router-link to="#">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste
                        </router-link>
                    </div>
                </div>
                 <div class="article-item">
                    <div class="article-img">
                        <img src="../assets/image/security-ilustration.svg" alt="">
                        <span class="likes"><box-icon name='heart' color="white" ></box-icon>34</span>
                        <span class="cat-title">Politics & Par</span>
                    </div>
                    <div class="article-title">
                        <router-link to="#">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste
                        </router-link>
                    </div>
                </div>
                 <div class="article-item">
                    <div class="article-img">
                        <img src="../assets/image/services3-ilustration.svg" alt="">
                        <span class="likes"><box-icon name='heart' color="white" ></box-icon>34</span>
                        <span class="cat-title">Politics & Par</span>
                    </div>
                    <div class="article-title">
                        <router-link to="#">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste
                        </router-link>
                    </div>
                </div>
                 <div class="article-item">
                    <div class="article-img">
                        <img src="../assets/image/services2-ilustration.svg" alt="">
                        <span class="likes"><box-icon name='heart' color="white" ></box-icon>34</span>
                        <span class="cat-title">Politics & Par</span>
                    </div>
                    <div class="article-title">
                        <router-link to="#">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste
                        </router-link>
                    </div>
                </div>
                 <div class="article-item">
                    <div class="article-img">
                        <img src="../assets/image/services1-ilustration.svg" alt="">
                        <span class="likes"><box-icon name='heart' color="white" ></box-icon>34</span>
                        <span class="cat-title">Politics & Par</span>
                    </div>
                    <div class="article-title">
                        <router-link to="#">
                            Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste
                        </router-link>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<script>
export default {
    name: 'ArticlesVue'
}
</script>
<style lang="scss" scoped>
    .article{
        padding: 4.5rem 0;
    }
    .article-content{
        margin: 1rem 0;
        @media screen and (min-width: 768px){
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 2rem;
        }
        @media screen and(min-width: 1200px){
            grid-template-columns: repeat(3, 1fr);
        }
    }
    .article-item{
        cursor: pointer;
        margin: 1.5rem 0;
        @media screen and(min-width: 768px) {
            margin: 0;
        }
    }
    .article-img{
        position: relative;
        overflow: hidden;

        &::after{
            position: absolute;
            content: '';
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.3);
        }
        &:hover{
            transform: scale(1.2);
        }
        img{
            transition: all 0.5s ease;
        }
    }

    .likes{
        position: absolute;
        display: flex;
        align-items: center;
        gap: 0.5rem;
        z-index: 1;
        top: 10px;
        left: 10px;
        background: var(--first-color);
        color: var(--container-color);
        padding: 0.25rem 1rem;
    }
    .cat-title{
        position: absolute;
        z-index: 1;
        bottom: 10px;
        right: 10px;
        color: var(--container-color);
        font-weight: 700;
        font-size: 1.1rem;
    }
    .article-title{
        padding: 1rem;
        font-size: 1.2rem;
        text-align: center;
        width: 70%;
        margin: 0 auto;

        a{
            text-transform: capitalize;
            color: var(--first-color);
        }
    }

</style>