<template>
    <div>
        <h1> Hello  {{ name }} also known as  {{ heroName }}  </h1>
    </div>
</template>

<script>
    export default {
        name: "GreatVue",
        data(){
            return{}
        },
        props : [
            "name",
            "heroName"
        ],
        methods:{

        },
        computed:{

        },
        watch:{

        },

    }
</script>

<style scoped>

</style>