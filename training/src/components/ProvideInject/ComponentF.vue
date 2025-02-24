<template>
    <div>
        <h1> Component F </h1>
        <h2> Compoent F username from Component App by provide/inject : {{ username }} </h2>
    </div>
</template>

<script>
    export default {
        name : "ComponentF",
        inject: [
            "username"
        ]
    }
</script>

<style scoped>

</style>