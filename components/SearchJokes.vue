<template>
    <form @submit.prevent="onSubmit">
        <input type="text" v-model="text" placeholder="Search Jokes..."/>
        <button type="submit"><i class="fas fa-search"></i></button>
    </form>
</template>

<script>
export default {
    name : 'SearchJokes',
    data(){
        return{
            text : ''
        }
    },
    methods:{
        onSubmit(){
            this.$emit('search-text',this.text);
            this.text = "";
        }
    }
}
</script>

<style scoped>
    form{
        margin-top: .5rem;
        text-align: center;
    }
    input{
        padding: .5rem 1rem;
        border-radius: 5px;
        border: 1px solid #242d3f;
    }
    button{
        transition: .25s;
        background-color: #242d3f;
        border-radius: 5px;
        border: 0;
        color: white;
        padding: .5rem .75rem;
        cursor: pointer;
    }
    button:hover{
        background-color: #7997d4;
    }
    button i{
        color: white;
    }
    
</style>