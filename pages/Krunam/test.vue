<template>
    <div>
        <h1>Welcome {{name}}</h1>
        <input type="text" :value="name">
        <input type="text" v-model="name">
        <h2> {{upperName}} </h2>
        <button @click="doSave">SAVE</button>
    </div>
</template>
<script>
export default {
    data(){
        return{
            name : "it"
        }
    },
    computed:{
        upperName(){
            return this.name.toUpperCase()
        }
    },
    methods:{
        doSave(){
            console.log("SAVE");
        },
    },
}
</script>