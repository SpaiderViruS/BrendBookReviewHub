<template>
  <section class="tone">
    <h2>Тональность общения</h2>
    <p class="description">
      Стиль коммуникации с пользователями: дружелюбный, честный, без токсичности.  
      Мы за свободу мнений — но без хамства.
    </p>

    <div class="grid">
      <div class="tone-card good">
        <h3>Можно</h3>
        <ul>
          <li>«Не зашло, но визуал классный»</li>
          <li>«Запутанный сюжет, но есть интересные мысли»</li>
          <li>«Один из лучших персонажей, которых я видел»</li>
          <li>«Фанатам жанра точно понравится»</li>
        </ul>
      </div>

      <div class="tone-card bad">
        <h3>Нельзя</h3>
        <ul>
          <li>«Тупое говно для деградов»</li>
          <li>«Автор идиот, кто это вообще снял»</li>
          <li>«Смотреть — трата времени, сжечь это»</li>
          <li>«Если тебе понравилось — тебе к врачу»</li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.tone {
  margin-top: 40px;
}

.tone h2 {
  font-size: 1.5em;
  color: #e94560;
  margin-bottom: 0.5em;
}

.description {
  margin-bottom: 1.5em;
  color: #c4c4c4;
  max-width: 600px;
}

.grid {
  display: flex;
  flex-wrap: wrap;
  gap: 24px;
}

.tone-card {
  flex: 1 1 300px;
  padding: 16px;
  border-radius: 10px;
  background-color: #2a2a40;
}

.tone-card.good {
  border-left: 6px solid #4caf50;
}

.tone-card.bad {
  border-left: 6px solid #f44336;
}

.tone-card h3 {
  color: #ffffff;
  margin-bottom: 10px;
}

.tone-card ul {
  padding-left: 20px;
  color: #dddddd;
}

.tone-card li {
  margin-bottom: 6px;
}
</style>
