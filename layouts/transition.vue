<!--
  轉場/特殊頁 — 白底
-->
<template>
  <div class="slide-transition">
    <div class="top-bar"></div>
    <div class="transition-content">
      <slot />
    </div>
  </div>
</template>

<style scoped>
.slide-transition {
  width: 100%;
  height: 100%;
  background: #FAFAFA !important;
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

.transition-content {
  position: relative;
  z-index: 1;
  padding: 80px 100px;
  height: 100%;
}

.transition-content :deep(h1) {
  color: #0F172A;
  font-family: 'Space Grotesk', 'Noto Sans TC', sans-serif;
  font-size: 3rem;
  font-weight: 800;
  line-height: 1.2;
  margin: 0 0 20px 0;
}

.transition-content :deep(p) {
  color: #475569;
  font-family: 'Manrope', 'Noto Sans TC', sans-serif;
  font-size: 1.05rem;
  line-height: 1.6;
}
</style>
