<template>
  <header class="page-header">
    <div class="page-header__images">
      <img
        v-for="(i, k) in [1,2,3,4]"
        :key="k"
        class="page-header__images__image"
        :src="`/img/${i}.jpg`">
    </div>
    <span>Welcome to my website!</span> 
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


.page-header
  text-align: center
  ul
    @include stripped-ul
  li
    display: inline
  &__images
    display: grid
    grid-template-columns: repeat(4, 1fr)
    grid-column-gap: 0.2em
    &__image
      width: 100%
</style>
