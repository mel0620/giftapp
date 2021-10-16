<template>
  <main>
    <div class="wrapper" v-if="post">
      <h1>TEST</h1>
      <p style="color: white">{{ post.createdAt }}</p>
      <p style="color: white">{{ post.title }}</p>
      <nuxt-content :document="post" />
    </div>
  </main>
</template>

<script>
export default {
  async asyncData({ $content, params, error }) {
    let post
    try {
      post = await $content('activities', params.activities).fetch()
    } catch (e) {
      error({ message: 'Post not found' })
    }
    return { post }
  },
  methods: {
    formatDate(dateString) {
      const date = new Date(dateString)
      return date.toLocaleDateString(process.env.lang) || ''
    },
  },
}
</script>
