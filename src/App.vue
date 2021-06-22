<template>
    <ul>
        <learning-resource
                v-for="resource in storedResources"
                :key="resource.id"
                :title="resource.title"
                :description="resource.description"
                :link="resource.link"
        >
        </learning-resource>
    </ul>
</template>

<script>

    import LearningResource from './components/learning-resources/LearningResource';

    export default{
      components:{
        LearningResource
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
