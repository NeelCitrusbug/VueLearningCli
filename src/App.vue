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

  <!-- <Input v-model="name"/> -->

  <!-- <Card/>

  <Card>
    Card content
  </Card>
  <Card>
    <h2>Card content</h2> 
  </Card>

  <Card>
    <img src="https://picsum.photos/200" alt="img">
  </Card>

  <Card>
    <template v-slot:header>
      Header
    </template>
    <template v-slot:default>
      <img src="https://picsum.photos/200" alt="img">
    </template>
    <template v-slot:footer>
      Details
    </template>
    
  </Card> -->

  <!-- <NameList>
      <template v-slot:default="slotProps">
        {{ slotProps.firstName }} {{ slotProps.lastName }}
      </template>
  </NameList> -->

  <h4>App component text</h4>
  <ChildeStyles>
    <h4>Childe Styles component text</h4>
  </ChildeStyles>

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

// import Input from './components/InputComp.vue'
// import Card from './components/CardComp.vue'
// import NameList from './components/NameList.vue'
import ChildeStyles from './components/ChildeStyles.vue'

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
    // Input,
    // Card,
    // NameList,
    ChildeStyles,
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

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
h4{
  color:orange;
}
</style>
