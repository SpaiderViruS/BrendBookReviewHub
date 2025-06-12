<template>
  <section class="usage">
    <h2>Примеры использования</h2>
    <p class="description">
      Ниже представлены примеры того, как бренд используется в реальных интерфейсах и визуальных элементах: карточки, баннеры, оформление постов.
    </p>

    <div class="grid">
      <div class="example" v-for="ex in examples" :key="ex.title">
        <div class="preview">
          <img :src="ex.img" :alt="ex.title" />
        </div>
        <h3>{{ ex.title }}</h3>
        <p class="note">{{ ex.note }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
const examples = [
  {
    title: 'Карточка фильма',
    img: new URL('@/assets/examples/FilmCard.png', import.meta.url).href,
    note: 'Отображает постер, название и рейтинг'
  },
  {
    title: 'Баннер с подборкой',
    img: new URL('@/assets/examples/Podborka.png', import.meta.url).href,
    note: 'Используется в промо или главной странице'
  },
  {
    title: 'Мобильный интерфейс',
    img: new URL('@/assets/examples/MobileView.png', import.meta.url).href,
    note: 'Версия сайта для смартфонов'
  }
]
</script>

<style scoped>
.usage {
  margin-top: 40px;
}

.usage h2 {
  font-size: 1.5em;
  color: #e94560;
  margin-bottom: 0.5em;
}

.description {
  margin-bottom: 1.5em;
  color: #c4c4c4;
}

.grid {
  display: flex;
  flex-wrap: wrap;
  gap: 24px;
}

.example {
  max-width: 240px;
  text-align: center;
}

.preview {
  width: 100%;
  height: 150px;
  overflow: hidden;
  border-radius: 12px;
  margin-bottom: 8px;
  background-color: #2a2a40;
  display: flex;
  align-items: center;
  justify-content: center;
}

.preview img {
  max-width: 100%;
  max-height: 100%;
  object-fit: cover;
  border-radius: 8px;
}

.note {
  font-size: 0.85em;
  color: #aaa;
}
</style>
