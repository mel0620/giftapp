<template>
  <main>
    <div class="proj"></div>
    <section v-if="posts" class="w-full max-w-5xl mx-auto">
      <h1 class="title">Projects</h1>
      <posts post-type="projects" :amount="10" />
    </section>
  </main>
</template>

<script>
export default {
  async asyncData({ $content, error }) {
    let posts
    try {
      posts = await $content('projects').fetch()
    } catch (e) {
      error({ message: 'Projects not found' })
    }
    return { posts }
  },
}
</script>

<style>
.proj {
  background-image: url('static/proj.jpg');
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
