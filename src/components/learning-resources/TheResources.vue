<template>
    <base-card>
        <base-button @click="setSelectedTab('stored-resources')" :mode="storedResourcesButtonMode">Stored Resources</base-button>
        <base-button @click="setSelectedTab('add-resource')" :mode="addResourceButtonMode">Add Resource</base-button>
    </base-card>
    <component :is="selectedTab"></component>
</template>

<script>

  import StoredResources from './StoredResources';
  import AddResource from './AddResource';

  export default {
    name: 'TheResources',
    data(){
      return {
        selectedTab:'stored-resources',
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
    },
    provide(){
      return {
        resources : this.storedResources
      }
    },
    methods:{
      setSelectedTab(tab){
        this.selectedTab = tab;
      }
    },
    components:{
      StoredResources,
      AddResource
    },
    computed:{
      storedResourcesButtonMode(){
        return this.selectedTab === 'stored-resources' ? null : 'flat'
      },
      addResourceButtonMode(){
        return this.selectedTab === 'add-resource' ? null : 'flat'
      }
    }
  };
</script>

<style scoped>

</style>
