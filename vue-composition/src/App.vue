<template>
    <div>
        <!-- <Data/> -->

        <!-- <DemoOne/> -->

        <!-- <Methods/> -->
        <!-- <VModel/> -->

        <!-- <Computed/> -->
        <!-- <Watch/> -->
        <!-- <ProvideInject/> -->
        <!-- <Lifecycle/> -->
        <!-- <TemplateRef/> -->
        <!-- <Person/> -->
        <ClickCounter/>
        <HoverCounter/>
    </div>
</template>

<script>
// import Data from './components/DataComp.vue'
// import Methods from './components/MethodsComp.vue'
// import VModel from './components/VModel.vue'
// import Computed from './components/ComputedComp.vue'
// import Watch from './components/WatchComp.vue'
// import ProvideInject from './components/ProvideInject.vue'
// import Lifecycle from './components/LifecycleC.vue'
// import TemplateRef from './components/TemplateRef.vue'
// import Person from './components/PersonComp.vue'
import ClickCounter from './components/ClickCounter.vue'
import HoverCounter from './components/HoverCounter.vue'

export default {
  name: 'App',
  components: {
    // Data,
    // DemoOne,
    // Methods,
    // VModel,
    // Computed,
    // Watch,
    // ProvideInject,
    // Lifecycle,
    // TemplateRef,
    // Person,
    ClickCounter,
    HoverCounter,
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
