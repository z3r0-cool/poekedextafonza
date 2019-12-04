<template>
<div class="search-box">
    <input type="text" name="" placeholder="Type to search" class="search-box" v-model="search">
    <a href="#" class="search-btn">

    </a>
</div>
</template>
<script>
export default {
    name: 'SearchBar',
    data(){
        return{
            search: '',

        }
    },
    computed: {
        filteredPokemons: function(){
            return [this.pokemons.filter((pokemon) =>{
                return pokemon.name.match(this.search);
            }
            )]
        }
    }
}
</script>

<style>
    .search-box{
        position: absolute;
        top: 4%;
        left: 50%;
        transform: translate(-50%, -50%);
        height: 20px;
        border-radius: 35px;
        padding: 10px;
    }
</style>