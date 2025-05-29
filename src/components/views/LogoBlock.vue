<!-- components/LogoBlock.vue -->
<template>
  <section class="logo-block">
    <h2>Логотип</h2>
    <p class="description">
      Основной логотип проекта и правила его использования.
    </p>

    <div class="logo-preview">
      <img :src="logoMain" alt="Основной логотип" />
      <p>Основной логотип на светлом фоне</p>
    </div>

    <div class="logo-variants">
      <div class="variant">
        <div class="bg light">
          <img :src="logoMain" alt="На светлом фоне" />
        </div>
        <p>На светлом фоне</p>
      </div>
      <div class="variant">
        <div class="bg dark">
          <img :src="logoMain" alt="На тёмном фоне" />
        </div>
        <p>На тёмном фоне</p>
      </div>
      <div class="variant forbidden">
        <div class="bg distorted">
          <img :src="logoMain" class="distorted" alt="Искажённый логотип" />
        </div>
        <p class="warn">Пример недопустимого использования</p>
      </div>
    </div>
  </section>
</template>

<script setup>
import logoMain from '@/assets/logo.png'
</script>

<style scoped>
.logo-block {
  margin-top: 40px;
}

.logo-block h2 {
  font-size: 1.5em;
  color: #e94560;
  margin-bottom: 0.5em;
}

.description {
  margin-bottom: 1.5em;
  color: #c4c4c4;
}

.logo-preview {
  text-align: center;
  margin-bottom: 2em;
}

.logo-preview img {
  max-width: 200px;
  max-height: 200px;
  object-fit: contain;
}

.logo-variants {
  display: flex;
  flex-wrap: wrap;
  gap: 24px;
  justify-content: space-around;
}

.variant {
  text-align: center;
  max-width: 200px;
}

.bg img {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
}

.bg {
  padding: 12px;
  border-radius: 8px;
  margin-bottom: 8px;
  height: 120px;
  width: 120px;
  background-color: #2f2f2f;
  display: flex;
  align-items: center;
  justify-content: center;
}

.bg.light {
  background-color: #f0f0f0;
}

.bg.dark {
  background-color: #1e1e2f;
}

.bg.distorted {
  background-color: #2f2f2f;
}

img.distorted {
  transform: rotate(15deg) scaleX(1.3);
  opacity: 0.6;
}

.warn {
  color: #ff4444;
  font-weight: bold;
}
</style>
