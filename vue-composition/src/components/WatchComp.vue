<template>
    <div>
        <input type="text" placeholder="first Name" v-model="fName">
        <input type="text" placeholder="last Name" v-model="lName">

        <input type="text" placeholder="Reactive first Name" v-model="firstName">
        <input type="text" placeholder="Reactive last Name" v-model="lastName">
        <input type="text" placeholder="Reactive hero Name" v-model="options.heroName">
    </div>
</template>

<script>
import {ref,watch,reactive,toRefs} from 'vue'
import _ from 'lodash'
    export default {
        name:'WatchComp',
        setup(){
            const fName = ref('')
            const lName = ref('')

            watch([fName,lName],(newValue,oldValue) => {
                console.log("oldValue fName",oldValue[0])
                console.log("newValue fName",newValue[0])
                console.log("oldValue lName",oldValue[1])
                console.log("newValue lName",newValue[1])
            },{
                immediate: true,
            })

            const state = reactive({
                firstName:'',
                lastName:'',
                options:{
                    heroName:''
                }
            })

            // watch(() => {
            //     return {...state}
            // },(newValue,oldValue) => {
            //     console.log("oldValue fName",oldValue?.firstName)
            //     console.log("newValue fName",newValue?.firstName)
            //     console.log("oldValue lName",oldValue?.lastName)
            //     console.log("newValue lName",newValue?.lastName)
            // },{
            //     immediate:true,
            // })

            //watching individual item

            watch(() => _.cloneDeep(state.options),(newValue,oldValue) => {
                console.log("oldValue fName",oldValue)
                console.log("newValue fName",newValue)
            },{
                immediate:true,
                deep:true,
            })

            return {
                fName,
                lName,
                ...toRefs(state),
            }
        }
    }
</script>

<style scoped>

</style>