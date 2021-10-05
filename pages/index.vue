<template>
  <div>
    <h3>This is my first web app using nuxtJs :)</h3>
    <p>Check the jokes from <nuxt-link to="/jokes">here .</nuxt-link></p>

  </div>
</template>

<script>
export default {
  head(){
    return{
      title: 'Home',
      meta : [
        {
          hid : 'description',
          name : 'description',
          content : 'This is home'
        }
      ]
    }
  }
}
</script>

<style>
  p a{
   color: #7997d4; 
  }
</style>