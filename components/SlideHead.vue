<script setup>
defineProps({
  num: { type: String, required: true },
  icon: { type: String, required: true },
  color: { type: String, default: '#E0A43B' },
  title: { type: String, required: true },
  objectif: { type: String, default: '' },
})
</script>

<template>
  <div class="shead">
    <div class="shead-left">
      <div class="sicon" :style="{ background: color }">
        <div :class="icon" />
      </div>
      <div class="snum">{{ num }}</div>
    </div>
    <div class="shead-main">
      <h2>{{ title }}</h2>
      <div v-if="objectif" class="pill">
        <span class="pill-label">Objectif visé</span>
        <span class="pill-text">{{ objectif }}</span>
      </div>
    </div>
  </div>
</template>
