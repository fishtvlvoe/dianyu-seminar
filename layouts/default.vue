<!--
  白底內容頁 — 頂部藍條 + 裝飾圓點
  大部分投影片使用此 layout
-->
<template>
  <div class="slide-default">
    <div class="top-bar"></div>
    <div class="deco-dot deco-dot-1"></div>
    <div class="deco-dot deco-dot-2"></div>
    <div class="slide-content">
      <slot />
    </div>
  </div>
</template>

<style scoped>
.slide-default {
  width: 100%;
  height: 100%;
  background: var(--bg-light, #FAFAFA);
  position: relative;
  overflow: hidden;
}

.slide-content {
  position: relative;
  z-index: 1;
  padding: 80px 100px;
  height: 100%;
}

.slide-content :deep(h1) {
  color: var(--text-heading, #0F172A);
  font-size: 3rem;
  font-weight: 800;
  line-height: 1.15;
  margin: 0 0 20px 0;
  letter-spacing: -0.02em;
}

.slide-content :deep(p) {
  color: var(--text-body, #475569);
  font-size: 1.1rem;
  line-height: 1.5;
}

.slide-content :deep(ul) {
  list-style: none;
  padding: 0;
}

.slide-content :deep(li) {
  color: var(--text-body, #475569);
  font-size: 1.05rem;
  line-height: 1.8;
}
</style>
