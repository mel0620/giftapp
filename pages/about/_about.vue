<template>
  <div class="wrapper">
    <h1>{{ page.title }}</h1>
    <p>{{ page.description }}</p>
    <!-- <img :src="page.cover" alt="" /> -->
    <nuxt-content :document="page" />
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params, error }) {
    const slug = params.slug || 'about/file'
    const page = await $content(slug)
      .fetch()
      .catch((err) => {
        error({ statusCode: 404, message: 'Page not found' })
      })

    return {
      page,
    }
  },
}
</script>
