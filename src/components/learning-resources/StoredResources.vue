<template>
    <ul>
        <learning-resource
                v-for="resource in resources"
                :key="resource.id"
                :id="resource.id"
                :title="resource.title"
                :description="resource.description"
                :link="resource.link"
        >
        </learning-resource>
    </ul>
</template>

<script>

  import LearningResource from './LearningResource';

  export default {
    inject:['resources'],
    components:{
      LearningResource
    },
    name: 'StoredResources'
  };
</script>

<style scoped>
    ul {
        list-style: none;
        margin: 0;
        padding: 0;
        margin: auto;
        max-width: 40rem;
    }
</style>
