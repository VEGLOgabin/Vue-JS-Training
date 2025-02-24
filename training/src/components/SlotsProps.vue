<template>
    <div>
        <h1 v-for="name in names" :key="name.firstName" >
            <slot name = "slot1" :firstName = "name.firstName" :lastName = "name.lastName"></slot>
        </h1>
    </div>
</template>

<script>
    export default {
        name : "NameList",
        data(){
            return {
                names : [
                    {
                        firstName : "Gobert",
                        lastName : "DODO"
                    },
                    {
                        firstName : "Bibi",
                        lastName : "GROTE"
                    },
                    {
                        firstName : "Bobo",
                        lastName : "TOGBE"
                    }
                ]
            }
        }
    }
</script>

<style scoped>

</style>