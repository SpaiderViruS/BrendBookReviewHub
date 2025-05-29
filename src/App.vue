<template>
  <div class="brandbook-wrapper">
    <main class="brandbook">
      <Intro />
      <ColorPalette />
      <Typography />
      <LogoBlock />
      <VisualElements />
      <ToneOfVoice />
      <UsageExample />
    </main>
  </div>
</template>

<script setup>
import Intro from './components/views/Intro.vue';
import ColorPalette from './components/views/CollorPallete.vue';
import Typography from './components/views/Typography.vue';
import LogoBlock from './components/views/LogoBlock.vue';
import VisualElements from './components/views/VisualElements.vue';
import ToneOfVoice from './components/views/ToneOfVoice.vue';
import UsageExample from './components/views/UsageExample.vue';
</script>

<style scoped>
.brandbook {
  max-width: 800px;
  margin: 0 auto;
  padding: 32px 16px;
  font-family: 'Segoe UI', sans-serif;
  line-height: 1.6;
  color: #fff;
  background-color: #1e1e2f;
  
}
.brandbook-wrapper {
  background: radial-gradient(ellipse at center, #2a2a40 0%, #1e1e2f 100%);
  background-attachment: fixed;
  min-height: 100vh;
  padding: 64px 0;
}
</style>
