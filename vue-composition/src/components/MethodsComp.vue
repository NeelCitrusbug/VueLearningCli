<template>
    <div>
        <h2>{{ counter }}</h2>
        <button @click="incrementCount">Increment Counter</button>

        <h2>{{ fName }} {{ lName }}</h2>
        <button @click="changeName">Change Name</button>
    </div>
</template>

<script>
import {ref,reactive,toRefs} from 'vue'
    export default {
        name:'MethodComp',
        setup(){
            const counter = ref(0)

            function incrementCount(){
                counter.value++
            }

            const state = reactive({
                fName:'Bruce',
                lName:'Wayne'
            })

            function changeName(){
                state.fName = 'Clerk'
                state.lName = 'Kent'
            }

            return {
                counter,
                incrementCount,
                ...toRefs(state),
                changeName
            }
        }
    }
</script>

<style scoped>

</style>