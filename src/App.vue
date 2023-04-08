<script>
import AppFooter from "./components/AppFooter.vue";
import AppHeader from "./components/AppHeader.vue";
import ComicsList from "./components/ComicsList.vue";

export default {
  components: {
    AppHeader,
    AppFooter,
    ComicsList,
  },
};
</script>

<template>
  <AppHeader />

  <main>
    <ComicsList />
  </main>

  <AppFooter />
</template>

<style lang="scss">
@use "./styles/general.scss";
</style>