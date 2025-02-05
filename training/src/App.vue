<template>

  <div>
    <div>
      <!-- <ListRendering /> -->
    </div>

    <div>
      <!-- <EventHandling /> -->
    </div>

    <div>
      <!-- <formHandling/> -->
    </div>

    <div>
      <!-- <computed-properties/> -->
    </div>

    <div>
      <!-- <WatchersVue/> -->
    </div>

    <div>
      <!-- <GreatVue name ="Gabin H. VEGLO"  heroName="The BOSS" />
      <hr>
      <GreatVue :name="name"  :heroName="channel" /> -->
    </div>


    <div>
      <ArticleVue title = "New Venue this new year" :likesNum="561" :isPublished="true" />
    </div>
    
  </div>


</template>

<script>
import ArticleVue from './components/PropsVue.vue';
// import GreatVue from './components/GreatVue.vue';

// import WatchersVue from './components/Watchers.vue';


// import ListRendering from './components/Component1.vue'
// import EventHandling from './components/EventHandling.vue'
// import FormHandling from "./components/FormHandling.vue"
// import ComputedProperties from "./components/ComputedProperties.vue"


export default {
  name: 'App',
  components: {
    // ListRendering,
    // EventHandling,
    // FormHandling,
    // ComputedProperties,
    // WatchersVue,
    // GreatVue,
    ArticleVue,
  },
  data(){
    return {
      name : "Gabbro TAKA",
      channel : "The GEEK",
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
