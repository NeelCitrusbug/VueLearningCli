<template>
    <div>
        <h2>{{ greet }}</h2>
        <button @click="sendEvent">Call Heros</button>
    </div>
</template>

<script>
import {computed} from 'vue'
    export default {
        name:'PersonGreeting',
        props: ['firstName', 'lastName'],
        // emits: ['callHeroes'],
        setup(props, context){
            console.log(context)
            const greet = computed(() => {
                return `${props.firstName} ${props.lastName}`
            })

            function sendEvent(){
                context.emit('callHeros',greet.value)
            }

            return {
                greet,
                sendEvent
            }
        }
    }
</script>

<style scoped>

</style>