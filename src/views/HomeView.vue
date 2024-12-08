<template>
  <div class="home">
    <h1>Home</h1>
    <!-- Passing posts array to the PostList component -->
    <PostList :post="posts"/>
  </div>
</template>

<script>
import PostList from '../components/PostList';  // Importing the PostList component
import { ref } from 'vue';

export default {
  name: 'Home',
  components: {
    PostList
  },
  setup() {
    const posts = ref([
      {
        id: 1, title: 'Artikel pertama di februari',
        body: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
      },
      {
        id: 2, title: 'Artikel kedua di februari',
        body: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
      }
    ]);

    
  }
}
</script>

<style>

</style>
