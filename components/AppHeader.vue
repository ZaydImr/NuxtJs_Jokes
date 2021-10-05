<template>
    <header class="header">
        <nuxt-link to="/"><h1 class="title">Dad Jokes</h1></nuxt-link> 
        <ul>
            <li>
                <nuxt-link to="/">Home</nuxt-link>
            </li>
            <li>
                <nuxt-link to="/jokes">Jokes</nuxt-link>
            </li>
            <li>
                <nuxt-link to="/about">About</nuxt-link>
            </li>
        </ul>
    </header>
</template>

<script>
export default {
    name : 'AppHeader'
}
</script>

<style scoped>
.header{
    justify-content: space-between;
    display: flex;
    align-items: center;
    color: #242d3f;
    border-bottom: 2px solid #242d3f;
}
ul{
    display: flex;
    list-style: none;

}
ul li{
    font-size: large;
}
ul li a{
    transition: .2s;
    text-decoration: none;
    padding: .5rem;
}
ul li a:hover{
    background-color: #1b2230;
    color: white;
}
</style>