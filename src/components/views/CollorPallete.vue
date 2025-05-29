<template>
  <section class="palette">
    <h2>Цветовая палитра</h2>
    <p class="description">Основные и дополнительные цвета бренда. HEX и RGB указаны для использования в веб-разработке.</p>

    <div class="colors">
      <div
        v-for="color in colors"
        :key="color.name"
        class="color-card"
        :style="getCardStyle(color.hex)"
      >
        <span class="color-name">{{ color.name }}</span>
        <span class="color-hex">{{ color.hex }}</span>
        <span class="color-rgb">{{ color.rgb }}</span>
      </div>
    </div>
  </section>
</template>

<script setup>
const colors = [
  { name: 'Фон (Dark Base)', hex: '#1e1e2f', rgb: '30, 30, 47' },
  { name: 'Акцент (Coral Red)', hex: '#e94560', rgb: '233, 69, 96' },
  { name: 'Основной текст (White)', hex: '#ffffff', rgb: '255, 255, 255' },
  { name: 'Вторичный текст (Gray)', hex: '#c4c4c4', rgb: '196, 196, 196' },
  { name: 'Выделение (Dark Blue)', hex: '#0f3460', rgb: '15, 52, 96' }
]

function getContrastColor(hex) {
  const r = parseInt(hex.substr(1, 2), 16)
  const g = parseInt(hex.substr(3, 2), 16)
  const b = parseInt(hex.substr(5, 2), 16)
  const brightness = (r * 299 + g * 587 + b * 114) / 1000
  return brightness > 128 ? '#000' : '#fff'
}

function getCardStyle(hex) {
  return {
    backgroundColor: hex,
    color: getContrastColor(hex)
  }
}
</script>

<style scoped>
.palette {
  margin-top: 40px;
}

.palette h2 {
  font-size: 1.5em;
  margin-bottom: 0.5em;
  color: #e94560;
}

.description {
  margin-bottom: 1em;
  color: #c4c4c4;
}

.colors {
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
}

.color-card {
  width: 180px;
  height: 110px;
  border-radius: 8px;
  padding: 12px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  box-shadow: 0 2px 6px rgba(0,0,0,0.2);
  transition: transform 0.2s;
}

.color-card:hover {
  transform: scale(1.05);
}

.color-name {
  font-weight: bold;
}

.color-hex, .color-rgb {
  font-size: 0.9em;
}
</style>
