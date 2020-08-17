<template>
    <div>
        <p>{{recipe.title}}</p>
        <div>
            <img :src="recipe.thumbnail" alt="">
        </div>
        <div>
            {{recipe.previewText}}
        </div>
    </div>
</template>

<script>
    export default {
        name: "index",
        asyncData(context){
            return new Promise((resolve, reject) => {
                setTimeout(() => {
                    resolve({
                        recipe: [
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
                        ].find(el => el.id == context.params.id)
                    })
                }, 1500)
            })
        }
    }
</script>

<style scoped>

</style>
