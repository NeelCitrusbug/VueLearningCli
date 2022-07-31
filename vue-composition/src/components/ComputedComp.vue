<template>
    <div>
        <input type="text" placeholder="first Name" v-model="refFirstName">
        <input type="text" placeholder="last Name" v-model="refLastName">

        <h2>{{refFullName}}</h2>

        <input type="text" placeholder="first Name" v-model="reactiveFirstName">
        <input type="text" placeholder="last Name" v-model="reactiveLastName">

        <h2>{{reactiveFullName}}</h2>
    </div>
</template>

<script>
import {ref,computed,reactive,toRefs} from "vue"
    export default {
        name:'ComputedComp',

        setup(){
            const refFirstName = ref('')
            const refLastName = ref('')

            const refFullName = computed(() => {
                return `${refFirstName.value} ${refLastName.value}`
            })

            const state = reactive({
                reactiveFirstName:'',
                reactiveLastName:''
            })

            const reactiveFullName = computed(() =>{
                return `${state.reactiveFirstName} ${state.reactiveLastName}`
            })

            return {
                refFirstName,
                refLastName,
                refFullName,
                ...toRefs(state),
                reactiveFullName,
            }
        }
    }
</script>

<style scoped>

</style>