<template>
    <nuxt-link :to="'/jokes/'+id">
        <div class="joke">
            <p>{{joke}}</p>
        </div>
    </nuxt-link>
</template>

<script>
export default {
    name:'Joke',
    props : ['joke','id']
}
</script>

<style scoped>
.joke{
    transition: .25s;
    padding: .25rem 1rem;
    margin: .5rem 0;
    border: 1px dotted #242d3f;
}
.joke:hover{
    background-color: #7997d4;
    color: white;
    border: 1px solid #7997d4;
}
.joke:hover p{
    color: white;
}
</style>