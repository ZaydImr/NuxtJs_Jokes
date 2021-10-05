<template>
    <div>
        <SearchJokes @search-text="searchText" />
        <span v-if="!jokes.length" class="laoding"><i class="fas fa-circle-notch"></i></span>
        <Joke :key="joke.id" :joke="joke.joke" :id="joke.id" v-for="joke in jokes"/>
    </div>
</template>

<script>
import axios from 'axios';
import Joke from '../../components/Joke.vue';
import SearchJokes from '../../components/SearchJokes.vue';

export default {
    components:{
        Joke,
        SearchJokes
    },
    data(){
        return{
            jokes: []
        }
    },
    async created(){
        const config = {
            headers : {
                'Accept' : 'application/json'
            }
        };

        try{
            const res = await axios.get('https://icanhazdadjoke.com/search',config);
            this.jokes = res.data.results;
        }catch(err){
            console.log(err);
        }
    },
    methods:{
        async searchText(text){
            console.log('test');
            const config = {
                headers : {
                    'Accept' : 'application/json'
                }
            };
        
            try{
                const res = await axios.get('https://icanhazdadjoke.com/search?term='+text,config);
                this.jokes = res.data.results;
            }catch(err){
                console.log(err);
            }
        }
    }
}
</script>

<style>
    .laoding{
        margin-top: 1rem;
        font-size: xx-large;
        display: block;
        text-align: center;
        -webkit-animation:rotation 3s linear infinite;
        animation:rotation 3s linear infinite;
    }
    @keyframes rotation {
    from {
        transform: rotate(0deg);
    }
    to {
        transform: rotate(359deg);
    }
}
</style>