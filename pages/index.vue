<template>
  <div class="is-radiusless is-shadowless is-marginless is-paddingless">
    <Navbar />
    <section class="section">
      <div class="container">
        <h1 class="title">
          fb-pages-calendar
        </h1>
        <h2 class="subtitle">
          A simple app for displaying events from FB pages you don&#39;t want to
          miss
        </h2>
        <h3>
          {{ ip }}
        </h3>
      </div>
    </section>
  </div>
</template>

<script>
import Navbar from '~/components/Navbar.vue'

export default {
  components: {
    Navbar
  },
  async asyncData({ $axios }) {
    const ip = await $axios.$get('http://icanhazip.com')
    return { ip }
  },
  methods: {
    async fetchSomething() {
      const ip = await this.$axios.$get('http://icanhazip.com')
      this.ip = ip
    }
  }
}
</script>

<style>
.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
