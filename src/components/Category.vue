<template >
    <div class="container">
        <div class="list" >
            <router-link @click="openActive()" to="#" :class="isActive ? 'slink' : 'slink active'">
                <box-icon name='bowl-rice' class="svg"></box-icon>
                <h4>Crypto</h4>
            </router-link>
            <router-link @click="openActive()" to="#" class="slink">
                <box-icon name='news' class="svg"></box-icon>
                <h4>Politics</h4>
            </router-link>
            <router-link to="#" :class="isActive ? 'slink' : 'slink'">
                <box-icon name='cricket-ball' type='solid' class="svg"></box-icon>
                <h4>Sport</h4>
            </router-link>
            <router-link to="#" class="slink">
                <box-icon name='terminal' type='solid' class="svg"></box-icon>
                <h4>Tech</h4>
            </router-link>
        </div>
    </div>
</template>
<script>
export default {
    name: 'CategoryVue',
    data() {
        return {
            isActive: false,
        }
    },
    methods: {
        openActive(){
            this.isActive = !this.isActive
        }
    },
}
</script>
<style lang="scss" scoped>
    .list{
        display: flex;
        justify-content: center;
        margin: 2rem 0;
        @media only Screen and (max-width: 48em){
            margin: 1rem;
            flex-wrap: wrap;
        }
    }
    .slink{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        border-radius: 50%;
        margin-right: 2rem;
        text-decoration: none;
        background: linear-gradient(to right, var(--first-color), var(--first-color-lighten));
        width: 6rem;
        height: 6rem;
        cursor: pointer;
        transform: scale(0.8);
        h4{
            color: var(--container-color);
            font-size: 0.8rem;
        }
    }
    .svg{
        color: var(--container-color);
        font-size: 1.5rem;
    }
    .active{
         display: flex;
         flex-direction: column;
         justify-content: center;
         align-items: center;
         border-radius: 50%;
         margin-right: 2rem;
         text-decoration: none;
         background: linear-gradient(to right, rgb(184, 166, 207), rgb(200, 188, 201));
         width: 6rem;
         height: 6rem;
         cursor: pointer;
         transform: scale(0.8);
         h4{
             color: var(--first-color);
             font-size: 0.8rem;
         }
    }
</style>