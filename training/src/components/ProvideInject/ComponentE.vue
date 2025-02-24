<template>
    <div>
        <h1> Component E </h1>
        <ComponentF/>
    </div>
</template>

<script>
import ComponentF from './ComponentF.vue';

    export default {
        name : "ComponentE",
        components : {
            ComponentF
        }
    }
</script>

<style scoped>

</style>