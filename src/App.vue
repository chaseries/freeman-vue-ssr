<template>
  <div id="app">
    <app-header></app-header>
    <router-view></router-view>
  </div>
</template>

<script>
import AppHeader from "VUE_COMPONENT/shared/app-header/Index.vue";

export default {
  name: "app",
  components: {
    AppHeader
  }
};
</script>

<style lang="sass">
@import "~SASS/main";
</style>
