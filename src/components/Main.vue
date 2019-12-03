<template>

</template>
<script>
import axios from 'axios'
export default {
    name: 'Main',
    data(){
        return{

        }
    },
    methods: {

    },
    created(){
        axios.get('https://jsonplaceholder.typicode.com/todos/1').then(response => {
            console.log(response)
        })
    }
}


</script>

