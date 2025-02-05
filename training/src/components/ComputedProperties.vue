<template>
    <div>
        <h1> Full Name :  {{ firstName }}  {{ lastName }} </h1>
        <h1> Computed fullname:  {{ fullname }} </h1>

        <button @click="changeName" > Change name </button>

        <div v-for="item in items" :key="item.id" >
            <div v-if="item.price>2023">
                <h1> {{ item.title }} </h1>
                <h2> {{ item.price }} </h2>
                <hr>
            </div>
        </div>

        <h3> Computed properties rendering </h3>
        <div v-for="item in expensiveItems" :key="item.id" >
            
                <h1> {{ item.title }} </h1>
                <h2> {{ item.price }} </h2>
                <hr>
        </div>

        <h1>Direct Total Calculation in the HTML : {{ items.reduce((total, item) => (total = total+ item.price),0) }} </h1>


        <!-- The difference between computed and Method is that: Computed properties are cached but method is not -->

        <h1> Computed total : {{ total }} </h1>
        <h1> Method(function) Total: {{ getTotal() }}  </h1>    
        <button @click="items.push({id:5, title: 'Good Guys', price : 2026})" > Push Item </button>
    </div>

    

</template>

<script>
    export default {
        name: "ComputedProperties",
        data(){
            return{
                firstName : "Houetchenou Gabin",
                lastName : "VEGLO",
                items : [
                    {
                        id: 1,
                        title: 'Good Shop',
                        price: 2022
                    },
                    {
                        id: 2,
                        title: 'Globo Globo',
                        price: 2023
                    },
                    {
                        id: 3,
                        title: 'GlaGla',
                        price: 2024
                    },
                    {
                        id: 4,
                        title: 'BABASSA',
                        price: 2025
                    },
                ]
            }
        },
        methods : {
            getTotal(){
                return this.items.reduce((total, item) => (total = total+ item.price),0)
            },
            changeName(){
                this.fullname = "Gabbro TATA"
            }
        },
        computed : {
            fullname:{
                get(){
                     return `${this.firstName} ${this.lastName}`
                },
                set(values){
                    const names = values.split(" ")
                    this.firstName = names[0]
                    this.lastName = names[1]
                }
               
            },
            total(){
                return this.items.reduce((total, item) => (total = total+ item.price),0)
            },
            expensiveItems(){
                return this.items.filter(( item => item.price>2023 ))
            },
        },
    }
</script>

<style scoped>

</style>