<template>
  <main>
    <div class="wrapper" v-if="post">
      <h1>TEST</h1>
      <nuxt-content :document="post" />
    </div>
  </main>
</template>

<script>
export default {
  async asyncData({ $content, params, error }) {
    let post
    try {
      post = await $content('activities', params.project).fetch()
    } catch (e) {
      error({ message: 'Project not found' })
    }
    return { post }
  },
}
</script>
