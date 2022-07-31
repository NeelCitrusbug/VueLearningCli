<template>
    <div>
        <input type="text" placeholder="first name" v-model="firstName">
        <input type="text" placeholder="last name" v-model="lastName">
        <PersonGreeting 
            :firstName="firstName" 
            :lastName="lastName" 
            @callHeros = "callHeros"
        />
    </div>
</template>

<script>
import PersonGreeting from './PersonGreeting.vue'
import {ref} from 'vue'
    export default {
        name:'PersonComp',
        components: {
            PersonGreeting,
        },
        setup(){
            const firstName = ref('')
            const lastName = ref('')

            function callHeros(hero){
                alert(`Calling ${hero}`)
            }

            return {
                firstName,
                lastName,
                callHeros
            }
        }
    }
</script>

<style scoped>

</style>