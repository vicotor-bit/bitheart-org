<template>
  <footer>
    <div class="container">
      <p>&copy; {{ currentYear }} BitHeart.org. All rights reserved.</p>
    </div>
  </footer>
</template>

<script>
import { computed } from 'vue'

export default {
  name: 'SiteFooter',
  setup() {
    const currentYear = computed(() => new Date().getFullYear())
    return { currentYear }
  }
}
</script>

<style scoped>
footer {
  background-color: #2c3e50;
  color: #ffffff;
  padding: 20px 0;
  text-align: center;
}
</style>

