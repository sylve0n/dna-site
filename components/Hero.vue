<template>
  <section class="hero" :style="{ 'background-image': 'url(' + image + ')' }">
    <h1 class="title text-center" v-if="title">{{ title }}</h1>
    <h2 class="subtitle text-center h3" v-if="subtitle">{{ subtitle }}</h2>
  </section>
</template>

<script>
export default {
  name: 'Hero',
  props: {
    title: {
      type: String,
      default: '',
    },
    subtitle: {
      type: String,
      default: '',
    },
    image: {
      type: String,
      default: '',
    },
  },
}
</script>
<style lang="scss" scoped>
  .hero {
    padding: 76px 0.5rem 1rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    background-size: cover;
    background-position: center;
    height: 500px;
    max-height: 80vh;
    background-attachment: fixed;
    .title {
      margin-top: 0;
      margin-bottom: 0.5em;
    }
    @include breakpoint(medium) {
      padding: 76px 2rem 1rem;
    }
  }
</style>