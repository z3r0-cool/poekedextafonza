<template>
        <div class="navbar">
        <nav class="nav-wrapper">
            <div class="nav-content">
                <router-link to="">
                    <span class="nav-title">PokeMON</span>
                </router-link>
            </div>
        </nav>
    </div>
</template>
<script>
export default {
    name: 'Navbar',
    data(){
        return{

        }
    }
}
</script>

<style>
.navbar{
    background-color: #3b4cca;
    font-size: 1.8em;
    height: 70px;
    width: 100%;
    }
.navbar nav{
    padding: 0 20px;
}
a:link {
  text-decoration: none;
}

a:visited {
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

a:active {
  text-decoration: underline;
}
a{
    color: #fefefe;
}
</style>