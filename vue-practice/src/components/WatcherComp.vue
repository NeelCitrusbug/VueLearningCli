<template>
    <div>
        <h2>Volume Tracker(0-20)</h2>
        <h3>Current volume : {{volume}}</h3>
        <div>
            <button @click="volume-=2">Decrease</button>
            <button @click="volume+=2">Increase</button>
        </div>
        <input type="text" v-model="movie">
        <input type="text" v-model="movieInfo.title">
        <input type="text" v-model="movieInfo.actor">
        <div>
            <button @click="movieList.push('wonder women')">Add movie</button>
            <!-- <button @click="movieList = movieList.concat(['wonder women'])">Add movie</button> -->
        </div>
    </div>
</template>

<script>
    export default {
        name:'WatcherComp',
        data(){
            return{
                volume:0,
                movie:'bat',
                movieInfo:{
                    title:'',
                    actor:''
                },
                movieList:['Batman','Superman']
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
            },
            movie:{
                handler(newValue){
                    console.log(`api called - movie is ${newValue}`)
                },
                immediate:true,
            },
            movieInfo:{
                handler(newValue){
                    console.log(`api called - movie title is ${newValue.title} and actor is ${newValue.actor}`)
                },
                deep:true,
                immediate:true,
            },
            movieList:{
                handler(newValue){
                    console.log(`updated list is ${newValue}`)
                },
                deep:true,
                immediate:true,
            }  
        }
    }
</script>

<style scoped>

</style>