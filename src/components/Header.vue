<template>
  <header>
    <div class="container">
      <nav>
        <router-link to="/" class="logo">BitHeart.org</router-link>
        <!-- 可以删除或注释掉其他导航链接 -->
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'SiteHeader'
}
</script>

<style scoped>
header {
  background-color: #ffffff;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 0;
}

.logo {
  font-size: 24px;
  font-weight: bold;
  color: #3498db;
  text-decoration: none;
}

.nav-links a {
  margin-left: 20px;
  text-decoration: none;
  color: #2c3e50;
  transition: color 0.3s ease;
}

.nav-links a:hover {
  color: #3498db;
}
</style>

