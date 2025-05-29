<template>
  <section class="visual-elements">
    <h2>Графические элементы</h2>
    <p class="description">Фирменные иконки, стили иллюстраций и паттернов, дополняющие визуальную айдентику.</p>

    <div class="grid">
      <div class="element" v-for="el in elements" :key="el.title">
        <div class="preview" :style="{ backgroundColor: el.bg }">
          <img :src="el.img" :alt="el.title" />
        </div>
        <h3>{{ el.title }}</h3>
        <p class="note">{{ el.note }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
const elements = [
  {
    title: 'Геймпад',
    img: new URL('@/assets/icons/gamepad.png', import.meta.url).href,
    note: 'Используется в карточках игр',
    bg: '#0f3460'
  },
  {
    title: 'Книга',
    img: new URL('@/assets/icons/book.png', import.meta.url).href,
    note: 'Для раздела с визуальными новеллами / мангой',
    bg: '#1e1e2f'
  },
  {
    title: 'Хлопушка',
    img: new URL('@/assets/icons/clapper.png', import.meta.url).href,
    note: 'Обозначает фильмы и сериалы',
    bg: '#2a2a40'
  }
]
</script>

<style scoped>
.visual-elements {
  margin-top: 40px;
}

.visual-elements h2 {
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
  justify-content: flex-start;
}

.element {
  max-width: 180px;
  text-align: center;
}

.preview {
  width: 100%;
  height: 120px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 12px;
  overflow: hidden;
  margin-bottom: 8px;
}

.preview img {
  max-width: 80px;
  max-height: 80px;
}

.note {
  font-size: 0.85em;
  color: #aaa;
}
</style>
