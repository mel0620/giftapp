<template>
  <main>
    <div class="posts"></div>
    <section v-if="posts" class="w-full max-w-5xl mx-auto">
      <h1 class="title">Posts</h1>
      <posts post-type="blog" :amount="10" />
    </section>
  </main>
</template>

<script>
export default {
  async asyncData({ $content, error }) {
    let posts
    try {
      posts = await $content('blog').fetch()
    } catch (e) {
      error({ message: 'Posts not found' })
    }
    return { posts }
  },
}
</script>

<style>
.posts {
  background-image: url('static/posts.jpg');
  height: 40vh;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: top;
  /* background-attachment: fixed; */
  margin-top: -1rem;
  margin-left: -2rem;
  margin-right: -2rem;
  margin-bottom: 2rem;

  @media screen and (max-width: 426px) {
    height: 25vh;
  }
}
</style>
