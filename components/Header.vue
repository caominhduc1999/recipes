<template>
    <header>
        <nav>
            <ul>
                <li><nuxt-link to="/">Home </nuxt-link></li>
                <li><nuxt-link to="/recipes">Recipes </nuxt-link></li>
                <li><nuxt-link to="/about">About </nuxt-link></li>
            </ul>
        </nav>
    </header>
</template>

<script>
    export default {
        name: "Header"
    }
</script>

<style scoped>
    header{
        width: 100%;
        height: 30px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    ul{
        list-style: none;
        margin: 0;
        padding: 0;
        display: flex;
        justify-content: center;
        align-items: center;
    }
</style>
