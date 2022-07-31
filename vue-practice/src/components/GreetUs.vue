<template>
    <div>
        <h2>{{ name }} - {{ job }}</h2>
        <!-- <h2 v-pre>{{ name }} - {{ job }}</h2> -->
    </div>
</template>

<script>
    export default {
        name:'GreetUs',
        props:['name','job']
    }
</script>

<style scoped>

</style>