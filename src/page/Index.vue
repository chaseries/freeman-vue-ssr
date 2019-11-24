<template>
  <section class="page page-index">
    <nav class="page-index__nav">
      <ul>
        <li><router-link to="/about">About Me</router-link></li>
        <li><router-link to="/work">My Work</router-link></li>
        <li><router-link to="/contact">Contact</router-link></li>
      </ul>
    </nav>
  </section>
</template>

<script>

export default {
  name: "page-index"
};
</script>

<style lang="sass">
@import "~SASS/mixin/strip";
@import "~SASS/mixin/typo";

.page-index
  text-align: center
  &__nav
    @include font-level-3
  ul
    @include stripped-ul

</style>
