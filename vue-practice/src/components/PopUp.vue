<template>
    <div>
        <h2>This is pop up</h2>
        <input type="text" v-model="name">
        <button @click="$emit('close',name)">Close Popup</button>
    </div>
</template>

<script>
    export default {
        name:'PopUp',
        data(){
            return{
                name:''
            }
        },
        // emits:['close'],
        emits:{
            close:(name) => {
                if(!name){
                    return false
                }
                else{
                    return true
                }
            }
        }
    }
</script>

<style scoped>

</style>