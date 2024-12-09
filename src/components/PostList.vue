<template>
  <div class="post-list">
    <div v-for="post in posts" :key="post.id">
     <PostSingle :post="post"/>
    </div>
  </div>
</template>

<script>
import { onUnmounted, onMounted, onUpdated } from 'vue';  // Perbaiki 'onUnMounted' menjadi 'onUnmounted'
import PostSingle from './PostSingle.vue'

export default {
  props: ['posts'],
  components: {
     PostSingle
  },
  setup(props) {
      // Lifecycle hook 'onMounted'
      onMounted(() => console.log('component mounted'))
      onUnmounted(() => console.log('component unmounted'))  // Perbaiki di sini
      onUpdated(() => console.log('component updated'))
  },
}
</script>
