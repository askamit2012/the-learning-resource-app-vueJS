<template>
  <h1>The Resource Learning App</h1>
  <ul>
    <LearningResource
      v-for="resource in storedResources"
      :key="resource.key"
      :id="resource.id"
      :title="resource.title"
      :description="resource.description"
      :link="resource.link"
    />
  </ul>
</template>

<script>
import LearningResource from './components/learning-resources/LearningResource.vue';
export default {
  components: {
    LearningResource,
  },
  data() {
    return {
      storedResources: [
        {
          id: 'official-guide',
          title: 'Official Guide',
          description: 'The Official VueJS documentation.',
          link: 'https://vuejs.org',
        },
        {
          id: 'google',
          title: 'Google',
          description: 'Learn To Google...',
          link: 'https://google.com',
        },
      ],
    };
  },
};
</script>

<style scoped>
h1 {
  color: purple;
}
</style>
