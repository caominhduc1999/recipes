<template>
    <section class="recipes">

        <Recipe
            v-for="recipe in recipes"
            :key="recipe.id"
                :thumbnail="recipe.thumbnail"
                :title="recipe.title"
                :previewText="recipe.previewText"
                :id="recipe.id"
        />

    </section>
</template>

<script>
    import Recipe from "@/components/Recipe";

    export default {
        name: "index",
        components: {Recipe},
        asyncData(){
            return new Promise((resolve, reject) => {
                setTimeout(() => {
                    resolve({
                        recipes: [
                            {
                                id: "1",
                                title: "Title1",
                                previewText: 'previewText',
                                thumbnail: 'https://www.talkwalker.com/images/2020/blog-headers/image-analysis.png'
                            },
                            {
                                id: "2",
                                title: "Title2",
                                previewText: 'previewText',
                                thumbnail: 'https://www.talkwalker.com/images/2020/blog-headers/image-analysis.png'
                            },
                        ]
                    })
                }, 1500)
            })
        }
    }
</script>

<style scoped>
    .recipes{
        display: flex;
        justify-content: center;
        align-items: center;
        flex-flow: row wrap;
    }
</style>
