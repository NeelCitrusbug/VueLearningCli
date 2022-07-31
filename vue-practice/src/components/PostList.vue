<template>
    <div>
        <!-- <button @click="getPosts">Load Posts</button> -->
        <div v-for="post in posts" :key="post.id">
            <h3>{{ post.id }} {{ post.title }}</h3>
            <p>{{ post.body }}</p>
        </div>
    </div>
</template>

<script>
import axios from 'axios';
    export default {
        name:'PostList',
        data(){
            return{
               posts:[]
            }
        },
        methods:{
             getPosts(){
                    axios.
                    get("https://jsonplaceholder.typicode.com/posts")
                    .then((res) => {
                        this.posts = res.data
                        console.log(res.data)
                    })
                    .catch((err)=>{
                        console.log(err)
                    })
                }
        },
        created(){
            this.getPosts()
        }
    }
</script>

<style scoped>

</style>