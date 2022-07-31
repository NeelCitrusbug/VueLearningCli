<template>
    <div>
        <h2>Artical component</h2>
        <h2 v-bind="$attrs">Artical {{title}}</h2>
        <h2>Likes {{likes}}</h2>
        <h2>Published {{published?'Yes':'No'}}</h2>
    </div>
</template>

<script>
    export default {
        name:'AritcalComp',
        // props:['title','likes'],
        props:{
            title:{
               type:String,
               required:true, 
            },
            likes:Number,
            published:Boolean,
        },
        inheritAttrs:false,
    }
</script>

<style scoped>

</style>