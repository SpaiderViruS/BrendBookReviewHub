<template>
  <main class="brandbook">
    <section class="intro">
      <h1>Брендбук проекта "MediaRate"</h1>
      <p class="subtitle">Сайт отзывов на фильмы, сериалы, игры и аниме</p>

      <div class="section">
        <h2>Миссия</h2>
        <p>Создать единое, удобное и честное пространство для оценки и обсуждения медиа-контента.</p>
      </div>

      <div class="section">
        <h2>Ценности</h2>
        <ul>
          <li>Открытость</li>
          <li>Честность</li>
          <li>Уважение к мнению</li>
          <li>Удобство</li>
        </ul>
      </div>

      <div class="section">
        <h2>Целевая аудитория</h2>
        <p>Пользователи от 16 до 30 лет, интересующиеся современным медиа-контентом: кино, играми, аниме и сериалами.</p>
      </div>
    </section>
  </main>
</template>

<script setup>
name: "Intro"
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

.intro h1 {
  font-size: 2em;
  margin-bottom: 0.25em;
}

.subtitle {
  font-size: 1.2em;
  margin-bottom: 2em;
  color: #c4c4c4;
}

.section {
  margin-bottom: 2em;
}

.section h2 {
  font-size: 1.5em;
  margin-bottom: 0.5em;
  color: #e94560;
}

.section ul {
  padding-left: 1.2em;
  list-style: disc;
}
</style>
