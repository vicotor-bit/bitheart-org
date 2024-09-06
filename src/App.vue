<template>
  <div id="app">
    <SiteHeader />
    <router-view></router-view>
    <SiteFooter />
  </div>
</template>

<script>
import SiteHeader from './components/Header.vue'
import SiteFooter from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    SiteHeader,
    SiteFooter
  }
}
</script>

