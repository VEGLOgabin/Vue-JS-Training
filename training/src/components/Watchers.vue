<template>
    <div>
        <div>
            <h1> Volume tracker (0 - 20) </h1>
            <h2> Current volume : {{ volume }} </h2>
        </div>
            <br><br>
            <button @click="increase(2)" > increment by 2 </button>
            <br><br>
            <button @click="decrease(2)" > decrease by 2 </button>
        <div>
            <br><br>
            <label for="movie"> Movie </label>
            <input type="text" id="movie" v-model="movie" >
        </div>

        <div>
            <br><br>
            <label for="movieinfoactor"> Movie Info Actor</label>
            <input type="text" id="movieinfoactor" v-model="movieinfo.actor" >
        </div>

        <div>
            <br><br>
            <label for="movieinfotitle"> Movie Info Title</label>
            <input type="text" id="movieinfotitle" v-model="movieinfo.title" >
        </div>

        <div>
            <br><br>
            <button @click="movielist.push('VOVO')" > Add new movie </button>
        </div>
    </div>
</template>

<script>
    export default {
        name: "WatchersVue",
        data(){
            return {
                volume : 0,
                movie : "Pop up",
                movieinfo : {
                    title : "Popo",
                    actor : "Messi"
                },
                movielist : ["COCO", "TATA"]
            }
        },
        methods:{
            increase(value){
                this.increasevolume = value
            },
            decrease(value){
                this.decreasevolume = value
            }
        },
        computed:{
            increasevolume:{
                set(value){
                    this.volume += value
                }
            },
            decreasevolume:{
                set(value){
                    this.volume -= value
                }
            },

        },
        watch:{
            volume(newvalue, oldvalue){
                if( newvalue > oldvalue && newvalue===16){
                    alert("Listen to a high volume for a long time may damage your hearing")
                }
            },
            // movie(newvalue){
            //     console.log(`The Api is called and get ${newvalue} from the database`)
            // }
            movie:{
                handler(newvalue){
                    console.log(`The Api is called and get ${newvalue} from the database`)
                },
                immediate : true
            },

            movieinfo:{
                handler(newvalue){
                console.log(`The Api is called and get movie info  ${newvalue.title} -- ${newvalue.actor} from the database`)
            },
            deep : true
            },
            movielist:{
                handler(newvalue){
                console.log(`The Api is called and get movie list ${newvalue} from the database`)
            },
            deep : true
            }

        }      
    }
</script>

<style scoped>

</style>