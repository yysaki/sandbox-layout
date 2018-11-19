<template>
  <div class="container">
    <header>header</header>
    <main class="content">HolyGrail</main>
    <nav class="side-nav">nav</nav>
    <aside class="side-bar">side</aside>
    <footer>footer</footer>
  </div>
</template>
<script>
export default {
  name: 'HolyGrailGridLayout'
}
</script>
<style>
header {
  background: #3e62ad;
}

footer {
  background: #727171;
}

.side-nav,
.side-bar {
  background: #ebeff6;
}

.container {
  display: grid;
  grid-template-areas:
    'header header header'
    'sidebar content nav'
    'footer footer  footer';
  grid-template-columns: 150px 1fr 150px;
  grid-template-rows: 100px 1fr 30px;
  min-height: 100vh;
}

@media screen and (max-width: 600px) {
  .container {
    grid-template-areas:
      'header'
      'sidebar'
      'content'
      'nav'
      'footer';
    grid-template-columns: 100%;
    grid-template-rows: 100px 50px 1fr 50px 30px;
    min-height: 100vh;
  }
}

header {
  grid-area: header;
}

.content {
  grid-area: content;
}

.side-nav {
  grid-area: nav;
}

.side-bar {
  grid-area: sidebar;
}

footer {
  grid-area: footer;
}
</style>
