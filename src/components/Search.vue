<template >
    <form class="form section">
        <div>
            <box-icon name='search' class="svg"></box-icon>
            <input type="text">
        </div>
    </form>
</template>
<script>
export default {
    name: 'SearchVue'
}
</script>
<style lang="scss" scoped>
    .form{
        margin: 0rem 20rem;
        div{
            position: relative;
            width: 100%;
        }
        input{
            border: none;
            background: linear-gradient(to right, var(--first-color), var(--first-color-lighten));
            font-size: 1.5rem;
            color: var(--text-color);
            padding: 1rem 3rem;
            border-radius: 1rem;
            outline: none;
            width: 100%;
        }
        @media only Screen and (max-width: 62em){
            margin: 0 8rem;
        }
        @media only Screen and (max-width: 48em){
            margin: 1rem 1rem;
        }
    }
    .svg{
            position: absolute;
            top: 50%;
            left: 0%;
            transform: translate(100%, -50%);
            color: var(--gray);
    }
</style>