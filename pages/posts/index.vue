<template>
  <div class="posts-page">
    <PostList :posts="loadedPosts" />
  </div>
</template>

<script>

export default {
  // middleware: 'log',
  computed: {
    loadedPosts() {
      return this.$store.getters.loadedPosts
    }
  }
 /*  created() {
    this.$store.dispatch('setPosts', this.loadedPosts)
    // console.log(this.$store.getters.loadedPosts);

  } */
}
</script>

<style scoped>
  .posts-page {
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
