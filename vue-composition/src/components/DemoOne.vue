<template>
    <div>
        <h2>{{ firstName }} {{ lastName }}</h2>
    </div>
</template>

<script>
import {reactive, toRefs} from 'vue'
    export default {
        name:'DemoOne',

        setup(){
            const state = reactive({
                firstName: 'Bruce',
                lastName: 'Wayne'
            })

            // const state2 = reactive({
            //     firstName: 'Neel',
            //     lastName: 'Shah'
            // })

            setTimeout(() => {
                state.firstName = 'Clerk'
                state.lastName = 'Kent'
            },2000)

            return {
                ...toRefs(state),
                // ...toRefs(state2),
            }
        }
    }
</script>

<style scoped>

</style>