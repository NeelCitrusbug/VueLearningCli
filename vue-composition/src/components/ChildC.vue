<template>
    <div>
        <h2>Child Component C</h2>
        <h3>Child c username - {{ userName }}</h3>

        <h3>Child c Count - {{ childCount }}</h3>
        <h3>Child c Hero - {{ fName }} {{ lName }}</h3>

        <button @click="incrementCount">Increment count from child</button>
    </div>
  
</template>

<script>
import { inject, toRefs } from 'vue'
export default {
  name: 'ChildC',
  
  setup(){
      const userName = inject('username','default value')

        const childCount = inject('count',0)
        const childHero = inject('state',{})

        const incrementCount = inject('incrementCount')

      return {
          userName,
          childCount,
            ...toRefs(childHero),
            incrementCount
      }
  }
}
</script>

<style scoped>
</style>