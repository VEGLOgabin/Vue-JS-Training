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
      <!-- <ArticleVue title = "New Venue this new year" :likesNum="561" :isPublished="true" /> -->
    </div>

    <div>
      <!-- <h1> Component App username : {{ name }} </h1>
      <ComponentC/> -->
    </div>

    <div>
      <!-- <SlotsVue> <h1> Welcome to my app </h1> </SlotsVue>
      <SlotsVue> <h1> Welcome to my New app </h1> </SlotsVue>
      <SlotsVue> <h1> Welcome to my older app </h1> </SlotsVue>
      <SlotsVue> <h1> Welcome to my group app </h1> </SlotsVue>
      <SlotsVue> <img src="@/assets/211.jpg" alt="Maize"> </SlotsVue> -->
    </div>

    <div>
      <!-- <NamedSlots>
        <template v-slot:header >
          <h1>
            My header
          </h1>
        </template>

        <template v-slot:content >
          <img src="@/assets/211.jpg" alt="Maize">

        </template>

        <template v-slot:footer >
          <h1>
            My Card Footer
          </h1>
        </template>
      </NamedSlots> -->
    </div>

    <div>
      <NameList>
        <template v-slot:slot1 = "SlotsProps" >
          {{ SlotsProps.firstName }} {{ SlotsProps.lastName }}
        </template>
      </NameList>

      <hr>

      <NameList>
        <template v-slot:slot1 = "SlotsProps" >
          {{ SlotsProps.lastName }}  {{ SlotsProps.firstName }}
        </template>
      </NameList>

      <hr>

      <NameList>
        <template v-slot:slot1 = "SlotsProps" >
          {{ SlotsProps.lastName }}
        </template>
      </NameList>
      
    </div>
    
  </div>


</template>

<script>
import NameList from './components/SlotsProps.vue';
// import ComponentC from './components/ProvideInject/ComponentC.vue';
// import NamedSlots from './components/NamedSlots.vue';
// import SlotsVue from './components/SlotsVue.vue';

// import ArticleVue from './components/PropsVue.vue';
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
    // ArticleVue,
    // ComponentC,
    // SlotsVue,
    // NamedSlots,
    NameList,
  },
  data(){
    return {
      name : "Gabbro TAKA",
      channel : "The GEEK",
    }
  },
  provide()  {
   return {
    username : this.name,
   } 
  }
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
