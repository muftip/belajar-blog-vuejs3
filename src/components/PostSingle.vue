<template>
  <div class="post-single">
    <h3>{{ post.title }}</h3>
    <p>{{ snippet }}</p>
  </div>
</template>

<script>
import { computed } from 'vue';

export default {
  props: ['post'],  // Properti 'post' akan diterima dari komponen induk
  setup(props) {
    // Menggunakan computed untuk membuat snippet dari body post
    const snippet = computed(() => {
      return props.post.body.substring(0, 50) + '...'; // Potongan pertama dari body
    });

    return {snippet};
  }
};
</script>

<style scoped>

</style>
