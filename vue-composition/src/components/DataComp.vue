<template>
    <div>
        <h2>Name - {{ firstName }} {{lastName}}</h2>
        <h2>{{ greet }}</h2>

        <h2>Name - {{ state.firstName }} {{state.lastName}}</h2>
        <h2>{{ greetReact }}</h2>
    </div>
</template>

<script>
import {ref, reactive} from 'vue'
    export default {
        name:'DataComp',
        setup(){
            //using ref
            const firstName = ref('Bruce')
            const lastName = ref('Wayne')
            
            console.log(firstName)

            const greet = `Hello ${firstName.value} ${lastName.value}`

            //using reactive

            const state = reactive({
                firstName: 'Clerk',
                lastName:'Kent'
            })

            const greetReact = `Hello ${state.firstName} ${state.lastName}`

            return {
                firstName,
                lastName,
                greet,
                state,
                greetReact
            }
        }
    }
</script>

<style scoped>

</style>