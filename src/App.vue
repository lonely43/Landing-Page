<script setup lang="ts">
import Picture from './components/Picture.vue'
import MainText from './components/MainText.vue'
import FAQ from './components/FAQ/FAQ.vue'
import SocialMedia from './components/SocialMedia.vue'
import Projects from './components/Projects.vue'
</script>

<template>
  <div class="body">
    <Picture />

    <MainText />
 
    <FAQ />

    <SocialMedia />

    <Projects />
  </div>
</template>

<style lang="scss" scoped>
  .body{
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 2rem;

    background-color: var(--color-background);
  }
</style>
