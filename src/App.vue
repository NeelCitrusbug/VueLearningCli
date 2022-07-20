<template>
  <div>
  <!-- <Greet name="neel"/>
  <Greet name="krupal"/>
  <Greet name="paresh"/>
  <Greet :name="name" :job="job" /> -->
  
  <!-- <Artical id="my-artical" title='title' :likes='50' :published="true"/> -->
  <Form />
  </div>
</template>

<script>
// import Greet fro m './components/GreetUs.vue'
// import Artical from './components/ArticalComp.vue'
import Form from './components/FormHandling.vue'
export default {
  name: 'App',
  components: {
    // Greet,
    // Artical,
    Form
  },
  data(){
    return {
      name:'neel',
      job:'developer',
      formValues:{
        name:''
      }
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
