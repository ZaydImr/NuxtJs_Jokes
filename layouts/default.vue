<template>
    <div class="container">
        <AppHeader/>
        <Nuxt />
    </div>
</template>

<script>
import AppHeader from '../components/AppHeader.vue';

export default {
    components:{
        AppHeader
    },
    head(){
        return{
            link: [
                {
                    rel : 'preconnect',
                    href : "https://fonts.googleapis.com"
                },
                {
                    rel : 'preconnect',
                    href : 'https://fonts.gstatic.com',
                    crossorigin : true
                },
                {
                    href: 'https://fonts.googleapis.com/css2?family=Poppins:wght@100;300;400;500;600;700;800&display=swap',
                    rel: 'stylesheet'
                },
                {
                    rel: 'stylesheet',
                    href:'https://pro.fontawesome.com/releases/v5.10.0/css/all.css',
                    integrity:'sha384-AYmEC3Yw5cVb3ZcuHtOA93w35dYTsvhLPVnYs9eStHfGJvOvKxVfELGroGkvsg+p',
                    crossorigin:"anonymous"
                }
            ]
        }
    }
}
</script>

<style>
body{
    background-color: whitesmoke;
}
*{
    font-family: 'poppins';
}
.container{
    max-width: 1100px;
    margin: auto;
    background-color: white;
    padding: 0 1rem 1rem;
}
a{
    text-decoration: none;
    color: #242d3f;
}
</style>