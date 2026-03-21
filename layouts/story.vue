<!--
  故事/概念頁 — 白底 + 頂部藍條 + 左文右視覺區
-->
<script setup>
const props = defineProps({
  label: { type: String, default: '' },
  visualLabel: { type: String, default: '圖解區域' },
  visual: { type: [Boolean, String], default: true },
  num: { type: String, default: '' }
})
</script>

<template>
  <div class="slide-story">
    <div class="top-bar"></div>
    <div class="story-left">
      <p v-if="label" class="story-label">{{ label }}</p>
      <slot />
    </div>
    <div v-if="visual !== false" class="story-right">
      <slot v-if="$slots.right" name="right" />
      <div v-else class="visual-area">
        <span class="visual-area-label">{{ visualLabel }}</span>
      </div>
    </div>
  </div>
</template>

<style scoped>
.slide-story {
  width: 100%;
  height: 100%;
  background: #FAFAFA !important;
  display: flex;
  position: relative;
  overflow: hidden;
}

.top-bar {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 4px;
  background: #0369A1;
  z-index: 10;
}

.story-left {
  flex: 1;
  padding: 80px 60px 80px 100px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.story-label {
  font-family: 'Space Mono', monospace;
  color: #0369A1;
  font-size: 0.85rem;
  margin-bottom: 16px;
}

.story-right {
  flex: 0 0 420px;
  padding: 80px 60px 80px 0;
  display: flex;
  align-items: center;
}

.slide-story :deep(h1) {
  color: #0F172A;
  font-family: 'Space Grotesk', 'Noto Sans TC', sans-serif;
  font-size: 2.8rem;
  font-weight: 800;
  line-height: 1.15;
  margin: 0 0 24px 0;
  letter-spacing: -0.02em;
}

.slide-story :deep(p) {
  color: #475569;
  font-family: 'Manrope', 'Noto Sans TC', sans-serif;
  font-size: 1.05rem;
  line-height: 1.6;
}

.visual-area {
  width: 100%;
  height: 80%;
  background: #E2E8F0;
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.visual-area-label {
  color: #94A3B8;
  font-family: 'Manrope', 'Noto Sans TC', sans-serif;
  font-size: 1rem;
  font-weight: 500;
}
</style>
