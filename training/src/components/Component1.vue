<template>
    <div>
        <div>
            <h1>{{great}}</h1>
        </div>

        <div>
            <h2 v-for="(name, index) in names" :key="index">  {{index}} - {{ name }}</h2>
        </div>
        <div>
            <h3 v-for="(name, index) in fullnames" :key="index">  {{index}} - {{ name.first }}  {{ name.last }}</h3>
        </div>

        <div v-for="(actor, index) in actors" :key="index">
            <h2> {{ actor.name }} </h2>
            <p v-for="(action, index) in actor.actions" :key="index"> {{ action }} </p>
        </div>

        <!-- Object rendering with v-for  -->

        <div v-for="(value, key, index) in myInfo" :key="index">
            <h2> {{ index }} {{ key }}  {{ value }} </h2>
        </div>


        <!-- ---------------------------------------------------------- -->
        <!-- conditional rendering  -->
        <h1>Conditional rendering</h1>
        <div v-for="(name, index) in names" :key="index" >
            
            <h2 v-if="name == 'Bogota' ">
                    {{ name }}
            </h2>
        </div>

        <h2> Add method (2,5,9):  {{add(2,5,9)}} </h2>
        <h2> Add method (7,5,9):  {{add(7,5,9)}} </h2>
        <h2> Multiplyer method (7,8) : {{multiplyer(7,8)}} </h2>
        
    </div>






</template>

<script>
    export default {
        name : "ListRendering",
        data(){
           return {
                great: "Welcome my love",
                names : ["Gabin", "Bogota", "Harris"],
                fullnames : [
                    { first: "Gabin", last: "VEGLO" },
                    { first: "Bono", last: "GAGA" },
                    { first: "Gohou", last: "TOTO" },
                    { first: "Elephant", last: "GOGO" },
                ],
                actors:[
                    {
                        name : "Gabo VOVO",
                        actions : ["Propos", "Geeks"]
                    },
                    {
                        name : "Gbahi TATA",
                        actions : ["Troc", "Pam"]
                    }
                ],
                myInfo : {
                    name : "Root",
                    channel : "Cabo cabo",
                    course : "Vue 3"
                }

           } 
        },

        methods:{
            add(a, b, c){
                return a+b+c
            },
            multiplyer(a,b){
                return a*b
            }
        },
    }
</script>

<style scoped>

</style>