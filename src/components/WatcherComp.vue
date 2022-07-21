<template>
    <div>
        <h2>Volume Tracker(0-20)</h2>
        <h3>Current volume : {{volume}}</h3>
        <div>
            <button @click="volume-=2">Decrease</button>
            <button @click="volume+=2">Increase</button>
        </div>
    </div>
</template>

<script>
    export default {
        name:'WatcherComp',
        data(){
            return{
                volume:0,
            }
        },
        watch:{
            volume(newValue,oldValue){
                if(newValue === 16 && newValue > oldValue){
                    alert('Volume is too high')
                }
                if(newValue > 20 || newValue < 0){
                    this.volume = oldValue
                }
            }
        }
    }
</script>

<style scoped>

</style>