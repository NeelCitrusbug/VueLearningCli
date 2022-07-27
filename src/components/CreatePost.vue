<template>
    <div>
        <form @submit.prevent="createPost">
            <div>
                <label for="userId">userId</label>
                <input id="userId" type="text" v-model="formData.userId">
            </div>
            <div>
                <label for="title">title</label>
                <input id="title" type="text" v-model="formData.title">
            </div>
            <div>
                <label for="body">body</label>
                <input id="body" type="text" v-model="formData.body">
            </div>
            <button>Submit</button>
        </form>
    </div>
</template>

<script>
import axios from "axios"
    export default {
        name:'CreatePost',
        data(){
            return {
                formData:{
                    userId:'',
                    title:'',
                    body:'',
                }
            }
        },
        methods:{
            createPost(){
                axios
                .post("https://jsonplaceholder.typicode.com/posts",this.formData)
                .then((res)=>{
                    console.log(res.data)
                })
                .catch((err)=>{
                    console.log(err)
                })
            }
        }
    }
</script>

<style scoped>

</style>