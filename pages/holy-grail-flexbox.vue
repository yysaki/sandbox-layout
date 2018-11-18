<template>
  <div class="container">
    <header>header</header>
    <div class="holyGrail">
      <main class="content">HolyGrail</main>
      <nav class="side-nav">nav</nav>
      <aside class="side-bar">side</aside>
    </div>
    <footer>footer</footer>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style>
.container {
  display: -webkit-flex;
  display: flex;
  margin: 0;
  padding: 0;
  min-height: 100vh;
  flex-direction: column;
  text-align: center;
}

header,
footer {
  width: 100%;
  padding: 2% 0;
  font-size: 1.2rem;
  color: #fff;
  flex: 0;
}

header {
  background: #3e62ad;
}

footer {
  background: #727171;
}

.holyGrail {
  display: flex;
  flex: 1;
}

.content {
  flex: 1;
}

.side-nav,
.side-bar {
  width: 200px;
  background: #ebeff6;
}

.side-nav {
  order: -1;
}
</style>
