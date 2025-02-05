<template>
    <div>
        <h1> Article Component </h1>
        <h2>Article Title :  {{ title }} </h2>
        <h2> Likes Number : {{ likesNum }} </h2>
        <h2> Published {{ isPublished ? "Yes":"No" }} </h2>
    </div>
</template>

<script>
    export default {
        name: "ArticleVue",
        props : {
            title : {
                type: String,
                required : true,
                default : "Default title is rendered",
            },
            likesNum : Number,
            isPublished : Boolean,
        }
    }
</script>

<style scoped>

</style>