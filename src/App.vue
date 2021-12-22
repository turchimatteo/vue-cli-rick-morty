<template>
  <div id="app">
    <Header />

    <main>
      <CharactersList />
    </main>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import CharactersList from "./components/CharactersList.vue";

export default {
  name: "App",
  components: {
    Header,
    CharactersList
  },
};
</script>

<style lang="scss">
@import './style/general';
</style>
