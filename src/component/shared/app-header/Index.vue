<template>
  <header class="page-header">
    <div class="page-header__images">
      <img
        v-for="(i, k) in [1,2,3,4]"
        :key="k"
        class="page-header__images__image"
        :src="`/img/${i}.jpg`">
    </div>
    <span class="page-header__tagline">Welcome to my website!</span> 
    <nav v-if="!isIndex">
      <ul>
        <li><router-link to="/">Home</router-link></li>
        <li><router-link to="/about">About Me</router-link></li>
        <li><router-link to="/work">My Work</router-link></li>
        <li><router-link to="/contact">Contact</router-link></li>
      </ul>
    </nav>
  </header>
</template>

<script>

export default {
  name: "app-header",
  computed: {
    isIndex () {
      return this.$route.fullPath === "/" ? true : false;
    }
  }
};
</script>

<style lang="sass">
@import "~SASS/mixin/strip";
@import "~SASS/mixin/typo";

.page-header
  text-align: center
  &__tagline
    @include font-level-4
  &__images
    display: grid
    grid-template-columns: repeat(4, 1fr)
    grid-column-gap: 0.2em
    margin-bottom: 4em
    &__image
      width: 100%
  ul
    @include font-level-3
    @include stripped-ul
    margin-bottom: 4em
  li
    display: inline
    padding: 0 0.5em
</style>
