<template>
    <div>
        <h2>{{ fullName }}</h2>
        <button @click="setFullName()">Change name</button>
        <h2> Computed total price: {{ total }}</h2>
        <h2> Method total price: {{ totalPrice() }}</h2>
        <button @click="items.push({id:4,title:'Pc',price:400})">Add item</button>
        <div>

            <input type="text" v-model="country">
        </div>

        <template v-for="item in items" :key="item.id">
            <h2 v-if="item.price > 100">{{ item.title }} - {{ item.price }}</h2>
        </template>
        <h2 v-for="item in exptensiveItems" :key="item.id">{{ item.title }} - {{ item.price }}</h2>
    </div>
</template>

<script>
    export default {
        name:'CompProps',
        data(){
            return {
                firstName:'Neel',
                lastName:'Shah',
                items:[
                    {
                        id:1,
                        title:'Tv',
                        price:100
                    },
                    {
                        id:2,
                        title:'Phone',
                        price:200
                    },
                    {
                        id:3,
                        title:'Laptop',
                        price:300
                    },
                ],
                country:'',
            }
        },
        methods:{
            totalPrice(){
                console.log("method price runs")
                return this.items.reduce((total,curr) => {return total+=curr.price},0)
            },
            setFullName(){
                this.fullName = 'Bruce Wayne'
            }
        },
        computed:{
            fullName:{
                get(){
                    return this.firstName + ' ' + this.lastName
                },
                set(value){
                    const names = value.split(' ')
                    this.firstName = names[0]
                    this.lastName = names[1]
                }
            },
            total(){
                console.log("computed price runs")
                return this.items.reduce((total,curr) => {return total+=curr.price},0)
            },
            exptensiveItems(){
                return this.items.filter(item => item.price > 100)
            }
        },
    }
</script>

<style scoped>

</style>