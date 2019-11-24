<template>
  <section class="page-about">
    <div class="page-about__content">
      <p>
      Hi, my name is Freeman. I'm a game design student at UCSC, and I've been passionate about game development since my teenage years.
      </p>
      <p>
      For games, I can do level design, programming, and 3D arts. I also love (like, really love) computers and internet in general. Instead of throwing you a big chunk of text about my skills, I'd like to demonstrate what I've done, and how I do them, in the section of <router-link to="/work">my work</router-link>.
      </p>
    </div>
  </section>
</template>

<script>

export default {
  name: "page-about"
};
</script>

<style lang="sass">
@import "~SASS/mixin/layout";
@import "~SASS/mixin/typo";

.page-about
  @include font-level-2
  &__content
    @include padded-wrap(700px)
</style>
