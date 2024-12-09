<template>
  <div class="home">
    <h1>Home</h1>
    <PostList v-if="showPosts" :posts="posts" />
    <button @click="showPosts = !showPosts">Unmounted</button>
    <button @click="posts.pop()">delete post</button>
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
    const posts = ref([]);
    
   const load = async () => {
    let data = await fetch('http://localhost:3000/psosts')
    posts.value = await data.json
     }
   
     load()

    return { posts }
  }
}
</script>
