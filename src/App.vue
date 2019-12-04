<template>
  <div id="app">
    <Navbar/>
    <SearchBar/>
    <Main/>
    <router-view/>
    
  </div>
</template>

<script>
import Navbar from '@/components/Navbar'
import SearchBar from '@/components/SearchBar'
import Main from '@/components/Main'

export default {
  name: 'App',
    components: {
    Navbar,
    SearchBar,
    Main
  }
}
</script>

<style>
#app{
  margin: 0;
  padding: 0;
}

</style>
