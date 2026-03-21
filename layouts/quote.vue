<!--
  金句頁 — 白底 + 左側藍條 + 置中大字 + 底線
  對應 Pencil: C - Key Statement
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
  background: var(--bg-light, #FAFAFA);
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.quote-content {
  position: relative;
  z-index: 1;
  max-width: 65%;
}

.quote-content :deep(h1) {
  color: var(--text-heading, #0F172A);
  font-size: 3rem;
  font-weight: 800;
  line-height: 1.25;
  margin: 0;
}

.quote-content :deep(p) {
  color: var(--text-body, #475569);
  font-size: 1.1rem;
  margin-top: 24px;
}

/* 金句底線 */
.quote-content :deep(h1)::after {
  content: '';
  display: block;
  width: 300px;
  height: 6px;
  background: var(--brand, #0369A1);
  border-radius: 3px;
  margin: 32px auto 0;
}
</style>
