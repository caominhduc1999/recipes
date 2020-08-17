<template>
    <nuxt-link :to="'/recipes/' + id">
        <article class="recipe">
            <div class="thumbnail" :style="{backgroundImage: 'url(' + thumbnail + ')'}"></div>
            <h1>{{Title}}</h1>
            <p>{{previewText}}</p>
        </article>
    </nuxt-link>
</template>

<script>
    export default {
        name: "Recipe",
        props: [
            'thumbnail',
            'title',
            'previewText',
            'id'
        ]
    }
</script>

<style scoped>
    .recipe{
        box-sizing: border-box;
        width: 280px;
        padding: 8px;
        border: 1px solid black;
        box-shadow: 0px 2px 2px #ccc;
    }

    .thumbnail{
        background-position: center;
        background-size: cover;
        width: 100%;
        height: 200px;
    }
</style>
