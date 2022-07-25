<template>
  <div>
  <!-- <Greet name="neel"/>
  <Greet name="krupal"/>
  <Greet name="paresh"/>
  <Greet :name="name" :job="job" /> -->
  
  <!-- <Artical id="my-artical" title='title' :likes='50' :published="true"/> -->
  <!-- <Form /> -->
  <!-- <CompProps /> -->
  <!-- <WatcherComp/> -->


  <!-- <h2>App comp username {{ name }}</h2>
  <ComponentC/> -->

  <!-- <button @click="showPopup=true">Show Popup</button>
  <PopUp v-show="showPopup" @close="closePopUp" /> -->

  <Input v-model="name"/>

  </div>
</template>

<script>
// import Greet from './components/GreetUs.vue'
// import Artical from './components/ArticalComp.vue'
// import Form from './components/FormHandling.vue'
// import CompProps from './components/CompProps.vue'
// import WatcherComp from './components/WatcherComp.vue'
// import ComponentC from './components/ComponentC.vue'
// import PopUp from './components/PopUp.vue'

import Input from './components/InputComp.vue'

export default {
  name: 'App',
  components: {
    // Greet,
    // Artical,
    // Form,
    // CompProps,
    // WatcherComp,
    // ComponentC,
    // PopUp,
    Input
  },
  data(){
    return {
      name:'neel',
      job:'developer',
      formValues:{
        name:''
      },
      showPopup:false,
    }
  },
  methods:{
    closePopUp(name){
      this.showPopup = false;
      console.log("name",name)
    }
  },
  provide(){
    return{
        userName:this.name,
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
</style>
