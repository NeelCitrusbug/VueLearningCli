<template>
    <div>
        <input type="text" placeholder="hero Name" v-model="heroName">
        <input type="text" placeholder="first Name" v-model="fName">
        <input type="text" placeholder="last Name" v-model="lName">
    </div>
</template>

<script>
import {ref,reactive,toRefs} from 'vue'
    export default {
        name:'VModel',
        setup(){
            const heroName = ref('')

            const state = reactive({
                fName:'',
                lName:'',
            })

            return {
                heroName,
                ...toRefs(state)
            }
        }
    }
</script>

<style scoped>

</style>