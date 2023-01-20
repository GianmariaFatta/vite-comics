<script>
import AppHeader from './AppHeader.vue';
export default {
  components: {
    AppHeader: AppHeader,
  }
}
</script>

<template>
  <header>
    <AppHeader />
  </header>
  <main></main>
  <footer></footer>

</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: sans-serif;
}

body {
  background-color: #1C1C1C;
}

.container {
  max-width: 1048px;
  margin: 0 auto;
  border: 2px dashed darkred
}

header {
  background-color: #fff;
  width: 100%;
  height: 110px;



}

footer {
  background-color: #303030;
}
</style>