<!--
  金句頁 — 白底 + 左側藍條 + 置中大字 + 底線
-->
<template>
  <div class="slide-quote">
    <div class="left-bar"></div>
    <div class="deco-dot deco-dot-1"></div>
    <div class="deco-dot deco-dot-2"></div>
    <div class="quote-content">
      <slot />
    </div>
  </div>
</template>

<style scoped>
.slide-quote {
  width: 100%;
  height: 100%;
  background: #FAFAFA !important;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.left-bar {
  position: absolute;
  top: 0;
  left: 0;
  width: 8px;
  height: 100%;
  background: #0369A1;
  z-index: 10;
}

.deco-dot {
  position: absolute;
  border-radius: 50%;
  background: #0369A1;
  pointer-events: none;
}

.deco-dot-1 {
  width: 80px;
  height: 80px;
  opacity: 0.08;
  top: 100px;
  right: 120px;
}

.deco-dot-2 {
  width: 50px;
  height: 50px;
  opacity: 0.05;
  top: 160px;
  right: 70px;
}

.quote-content {
  position: relative;
  z-index: 1;
  max-width: 65%;
}

.quote-content :deep(h1) {
  color: #0F172A;
  font-family: 'Space Grotesk', 'Noto Sans TC', sans-serif;
  font-size: 3rem;
  font-weight: 800;
  line-height: 1.25;
  margin: 0;
}

.quote-content :deep(h1)::after {
  content: '';
  display: block;
  width: 300px;
  height: 6px;
  background: #0369A1;
  border-radius: 3px;
  margin: 32px auto 0;
}

.quote-content :deep(p) {
  color: #475569;
  font-family: 'Manrope', 'Noto Sans TC', sans-serif;
  font-size: 1.1rem;
  margin-top: 24px;
}
</style>
