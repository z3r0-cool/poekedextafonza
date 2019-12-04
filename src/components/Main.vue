<template>
    <div>
        <ul>
            <li v-for="pokemon in pokemons" :key="pokemon.name">{{pokemon.name}}</li>
        </ul>
    </div>
</template>
<script>
import axios from 'axios'
export default {
    name: 'Main',
    data(){
        return {
            pokemons: [],
            countPaginator: 0
        }
    },
    methods: {

    },
    created(){
        axios.get(`https://pokeapi.co/api/v2/pokemon?offset=${this.countPaginator}&limit=20`).then(response => {
            console.log(response.data.results)
            this.pokemons = response.data.results
        })
        // let request = {
        //     "count":964,
        //     "next":"https://pokeapi.co/api/v2/pokemon?offset=20&limit=20",
        //     "previous":null,
        //     "results":[
        //         { 
        //             "name":"bulbasaur",
        //             "url":"https://pokeapi.co/api/v2/pokemon/1/"
        //         },
        //         { 
        //             "name":"ivysaur",
        //             "url":"https://pokeapi.co/api/v2/pokemon/2/"
        //         },
        //     ]
        // }
        // this.pokemons = request.results

    }
}


</script>

