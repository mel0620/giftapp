<template>
  <div class="wrapper">
    <!-- <p>{{ fileContent }}</p> -->
  </div>
</template>

<script>
// import mdFile from './file.md'
export default {
  data() {
    return {
      fileContent: '',
    }
  },
  mounted() {
    this.getMDFile()
  },
  methods: {
    getMDFile() {
      //   this.fileContent = mdFile
    },
  },
}
</script>
