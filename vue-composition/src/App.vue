<template>
    <div>
        <!-- <Data/> -->

        <!-- <DemoOne/> -->

        <!-- <Methods/> -->
        <VModel/>
    </div>
</template>

<script>
// import Data from './components/DataComp.vue'
// import Methods from './components/MethodsComp.vue'
import VModel from './components/VModel.vue'

export default {
  name: 'App',
  components: {
    // Data,
    // DemoOne,
    // Methods,
    VModel,
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
