<template>
  <section class="visual-elements">
    <h2>Графические элементы</h2>
    <p class="description">Фирменные иконки, стили иллюстраций и паттернов, дополняющие визуальную айдентику.</p>

    <div class="grid">
      <div class="element" v-for="el in elements" :key="el.title">
        <div class="preview-icon" :style="{ backgroundColor: el.bg }">
          <i :class="`mdi ${el.icon}`"></i>
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
    title: 'Поиск',
    icon: 'mdi-magnify',
    note: 'Используется в верхней панели для поиска контента',
    bg: '#2a2a40'
  },
  {
    title: 'Рейтинг',
    icon: 'mdi-star',
    note: 'Отображает оценку пользователя к фильму или игре',
    bg: '#1e1e2f'
  },
  {
    title: 'Отзывы',
    icon: 'mdi-comment-text',
    note: 'Иконка используется для обозначения раздела отзывов',
    bg: '#0f3460'
  },
  {
    title: 'Категория "Игры"',
    icon: 'mdi-gamepad-variant',
    note: 'Визуально подчёркивает карточки с видеоиграми',
    bg: '#4b4b6d'
  },
  {
    title: 'Категория "Фильмы"',
    icon: 'mdi-movie-open',
    note: 'Обозначает медиа-файлы: кино, сериалы и т.п.',
    bg: '#5d2d4b'
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
  justify-content: center;
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

.preview-icon {
  width: 100%;
  height: 120px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 48px;
  color: white;
  border-radius: 12px;
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
