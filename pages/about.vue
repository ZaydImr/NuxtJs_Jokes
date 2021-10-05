<template>
    <div>
        <h3>About</h3>
        <div class="line" :key="item.key" v-for="item in items">
            <label :for="item.key">{{item.key}}</label>
            <p :id="item.key">{{item.value}}</p>
        </div>
        <div class="line" :key="link.key" v-for="link in links">
            <label :for="link.key">{{link.key}}</label>
            <a :id="link.key" :href="link.link" target="_blank"><i :class="link.class"></i> {{link.value}}</a>
        </div>
    </div>
</template>

<script>
export default {
    head(){
        return {
            title: 'About'
        }
    },
    data(){
        return{
            items : [
                {
                    key: 'Technologies',
                    value : 'NuxtJs'
                },
                {
                    key: 'Version',
                    value : '1.0.0'
                }
            ],
            links : [
                {
                    key: 'Developer',
                    value : 'Zayd EL IMRANI',
                    link: 'https://www.linkedin.com/in/zaydimr/'
                },
                {
                    key: 'Github repository',
                    value : 'Github',
                    class : 'fab fa-github',
                    link: 'https://github.com/ZaydImr/NuxtJs_Jokes'
                },
                {
                    key: 'Api url',
                    value : 'icanhazdadjoke',
                    link: 'https://icanhazdadjoke.com/api'
                }
            ]
        }
    }
};
</script>

<style >
*{
    color: #242d3f;
}
    .line  {
        transition: .3s;
        padding: .75rem 2rem; 
        display: flex;
        align-items: center;
    }
    .line label{
        flex-basis: 180px;
        font-weight: 600;
    }
    .line p {
        margin: 0;
    }
    .line a{
        transition: .2s;
    }
    .line a:hover,.line a:hover i{
        color: #7997d4;
        font-weight: 500;
        font-size: large;
    }
</style>