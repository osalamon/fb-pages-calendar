<template>
  <section class="section">
    <div class="container">
      <nav class="navbar">
        <div class="navbar-brand">
          <a class="navbar-item" href="https://bulma.io">
            <img
              src="https://bulma.io/images/bulma-logo.png"
              width="112"
              height="28"
            />
          </a>
        </div>
        <div class="navbar-menu">
          <div class="navbar-end">
            <!-- use router-link component for navigation. -->
            <!-- specify the link by passing the `to` prop. -->
            <!-- `<router-link>` will be rendered as an `<a>` tag by default -->
            <router-link to="/foo" class="navbar-item">Go to Foo</router-link>
            <router-link to="/bar" class="navbar-item">Go to Bar</router-link>
            <router-link to="/baz" class="navbar-item">Go to Baz</router-link>
          </div>
        </div>
        <router-view></router-view>
      </nav>
    </div>
  </section>
</template>

<script>
import VueRouter from 'vue-router'
import Vue from 'vue'

export default {
  components: {}
}

Vue.use(VueRouter)
</script>
