<template>
    <div>
        <h3>Parent component count {{ count }}</h3>
        <h3>Parent component hero {{ fName }} {{ lName }}</h3>
        <button @click="incrementCount">Increment count</button>
        <ChildA />
    </div>
  
</template>

<script>
import { provide,ref,reactive,toRefs } from 'vue'
import ChildA from './ChildA.vue'
export default {
  components: { ChildA },
  name: 'ProvideInject',

  setup(){
      provide('username','Neel')

      const count = ref(0)

      const state = reactive({
          fName:'Bruce',
          lName:'Wayne'
      })

        function incrementCount(){
            count.value++
        }

      provide('count',count)
      provide('state',state)
      provide('incrementCount',incrementCount)

      return {
          count,
          ...toRefs(state),
          incrementCount,
      }
  }
  
}
</script>

<style scoped>
</style>