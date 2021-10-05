<template>
    <div class="joke-id">
        <nuxt-link to="/jokes"><i class="fas fa-angle-left"></i> Back to jokes</nuxt-link>
        <h3>{{joke.joke}}</h3>
        <hr />
        <small>Joke ID : {{joke.id}}</small>
    </div>
</template>

<script>
import axios from 'axios'

export default {
    data(){
        return {
            joke : {}
        }
    }    ,
    async created(){
        const config = {
            headers:{
                'Accept' : 'application/json'
            }
        };
        try {
            const res = await axios.get('https://icanhazdadjoke.com/j/'+this.$route.params.id,config);
            this.joke = res.data;
        } catch (error) {
            console.log(error);
        }
    },
    head(){
        return{
            title : 'Joke'
        }
    }
}
</script>

<style>
    .joke-id{
        margin-top: 1rem;
    }
    .joke-id a:hover{
        color: #7997d4;
    }
</style>