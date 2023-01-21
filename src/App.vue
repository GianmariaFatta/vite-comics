<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
export default {
  components: {
    AppHeader: AppHeader,
    AppMain: AppMain
  }
}
</script>

<template>
  <AppHeader />
  <AppMain />

  <footer></footer>

</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}


a {
  color: #000;
  text-decoration: none;
}


body {
  background-color: #1C1C1C;
  font-family: sans-serif;
  font-family: 'Alegreya',
    serif;
  font-family: 'Domine',
    serif;
  height: 100vh;

}

.container {
  max-width: 1200px;
  margin: 0 auto;
  /* border: 2px dashed darkred */
}

img {
  max-width: 100%;
  height: auto;
}

li {
  list-style-type: none;
}
</style>