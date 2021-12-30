<template>
    <div>
        <h1>Get Data</h1>
        <br>
         <button v-on:click="store()">Get DAta</button><br><br>
        <button v-on:click="display()">Display data</button><br><br>
    </div>
</template>
<script>
// import axios from 'axios'
export default {

    name:"GetDAta",
    data(){
       return{
            users:{
                name:"",
                email:""
            },
            error:{
                name:"",
                email:""
            },
            data:[],
            persons:null,
            id: undefined,
            response:null
       }
    },
    methods:{
        
        store(){
            this.axios.get('http://localhost:8888/person/getAll')
            .then(data=>(this.persons=data.data))
        },
        display(){
            console.warn(this.persons)
        }
    },
    mounted(){
    //    this.axios.get('http://localhost:8888/person/getAll')
    //         .then(data=>(console.warn(data.data)))
    }
    
}
</script>
<style>
.name{
    color: red;
}
</style>

