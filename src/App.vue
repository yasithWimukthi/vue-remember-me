<template>
    <the-header title="RememberMe"></the-header>
    <stored-resources :resources="storedResources"></stored-resources>
</template>

<script>

    import StoredResources from './components/learning-resources/StoredResources';
    import TheHeader from './components/layouts/TheHeader';

    export default{
      components:{
        StoredResources,
        TheHeader
      },
      data(){
        return {
          storedResources:[
            {
              id:'vue-official-guide',
              title:'Vue Official Guide',
              description:'The official vue.js documentation.',
              link:'https://vuejs.org'
            },
            {
              id:'react-official-guide',
              title:'React Official Guide',
              description:'The official react documentation.',
              link:'https://reactjs.org/docs/'
            }
          ]
        }
      }
    }
</script>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap');

    * {
        box-sizing: border-box;
    }

    html {
        font-family: 'Roboto', sans-serif;
    }

    body {
        margin: 0;
    }
</style>
