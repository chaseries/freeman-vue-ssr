<template>
  <section class="page page-index">
    <nav>
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
@import "~SASS/main";

.page-index
  text-align: center

  ul
    list-style-type: none
    margin: 0
    padding: 0

</style>
