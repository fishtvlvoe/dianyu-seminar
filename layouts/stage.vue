<!--
  階段轉場頁 — 白底 + 置中
-->
<script setup>
const props = defineProps({
  stage: { type: [String, Number], default: '' },
  from: { type: String, default: '' },
  to: { type: String, default: '' },
  subtitle: { type: String, default: '' },
  note: { type: String, default: '' }
})
</script>

<template>
  <div class="slide-stage">
    <div class="top-bar"></div>
    <div class="stage-content">
      <div class="stage-line"></div>
      <p class="stage-label">階段 {{ stage }}</p>
      <h1 class="stage-title">{{ from }} → {{ to }}</h1>
      <p v-if="subtitle" class="stage-sub">{{ subtitle }}</p>
      <div class="stage-line"></div>
      <slot />
    </div>
  </div>
</template>

<style scoped>
.slide-stage {
  width: 100%;
  height: 100%;
  background: #FAFAFA !important;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  position: relative;
}

.top-bar {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 4px;
  background: #0369A1;
}

.stage-line {
  width: 200px;
  height: 2px;
  background: #E2E8F0;
  margin: 0 auto 24px;
}

.stage-label {
  font-family: 'Space Mono', monospace;
  color: #0369A1;
  font-size: 1rem;
  margin-bottom: 12px;
}

.stage-title {
  color: #0F172A;
  font-family: 'Space Grotesk', 'Noto Sans TC', sans-serif;
  font-size: 4.5rem;
  font-weight: 800;
  line-height: 1.1;
  letter-spacing: -2px;
  margin: 0 0 20px;
}

.stage-sub {
  color: #64748B;
  font-family: 'Manrope', 'Noto Sans TC', sans-serif;
  font-size: 1.05rem;
  margin-bottom: 24px;
}
</style>
