<!-- components/Typography.vue -->
<template>
  <section class="typography">
    <h2>Типографика</h2>
    <p class="description">Шрифты, используемые в интерфейсе, их размеры и стили.</p>

    <div class="type-sample">
      <p class="label">Основной шрифт:</p>
      <p class="value">Inter / Roboto / Open Sans</p>
    </div>

    <div class="type-sample">
      <p class="label">Заголовки</p>
      <p class="heading-sample">Это пример заголовка H1 — 32px, Bold</p>
    </div>

    <div class="type-sample">
      <p class="label">Подзаголовки</p>
      <p class="subheading-sample">Пример подзаголовка — 24px, Semibold</p>
    </div>

    <div class="type-sample">
      <p class="label">Основной текст</p>
      <p class="text-sample">Это пример основного текста — 16px, Regular</p>
    </div>

    <div class="type-sample">
      <p class="label">Подписи</p>
      <p class="caption-sample">Пример подписи — 12px, Light</p>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.typography {
  margin-top: 40px;
}

.typography h2 {
  font-size: 1.5em;
  color: #e94560;
  margin-bottom: 0.5em;
}

.description {
  margin-bottom: 1.5em;
  color: #c4c4c4;
}

.type-sample {
  margin-bottom: 1.5em;
}

.label {
  font-weight: bold;
  font-size: 0.9em;
  margin-bottom: 0.25em;
  color: #ffffff;
}

.value, .heading-sample, .subheading-sample, .text-sample, .caption-sample {
  background-color: #2a2a40;
  padding: 12px;
  border-radius: 6px;
  color: #ffffff;
}

.heading-sample {
  font-size: 32px;
  font-weight: bold;
}

.subheading-sample {
  font-size: 24px;
  font-weight: 600;
}

.text-sample {
  font-size: 16px;
  font-weight: 400;
}

.caption-sample {
  font-size: 12px;
  font-weight: 300;
}
</style>
