<template>
    <div>
        <div>
        <h1>Name : {{ name }}</h1>
        <button @click="changeName($event), increment(3)"> Click to change the name </button>
        </div>

        <div>
            <h1> Counter increment and decrement </h1>
            <h2> Counter : {{ counter }} </h2>
            <button  v-on:click=" increment(1) " > Increment counter by : 1 </button>  <br/>  <br/>
            <button  v-on:click=" increment(3) " > Increment counter by : 3 </button>  <br/>  <br/>
            <button  @click=" increment(5) " > Increment counter by : 5 </button>  <br/>  <br/>
            <button v-on:click=" descrement(1) " > decrement counter by : 1 </button> <br/>  <br/>
            <button v-on:click=" descrement(3) " > decrement counter by : 3 </button> <br/>  <br/>
            <button @click=" descrement(5) " > decrement counter by : 5 </button> <br/>  <br/>
        </div>
    </div>
</template>

<script>
    export default {
        name : "EventHandling",
        data(){
            return {
                name : "Gabin",
                counter : 0,
            }
        },

        methods : {
            increment(num){
                this.counter += num
            },
            descrement(num){
                this.counter -= num
            },

            changeName(event){
                this.name = "GOFOO"
                console.log("Event ",event)
            }
        }
        
    }
</script>

<style scoped>

</style>