<template>
    <div>
        <h2>Component F</h2>
        <h3>prop value is {{ userName }}</h3>
    </div>
</template>

<script>
    export default {
        name:'ComponentF',
        inject:['userName']
    }
</script>

<style scoped>

</style>