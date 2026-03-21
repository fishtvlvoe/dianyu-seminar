<!--
  白底內容頁 — 純白底，內容自行控制裝飾
-->
<template>
  <div class="slide-default">
    <slot />
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

.slide-default :deep(h1) {
  color: var(--text-heading, #0F172A);
  font-family: 'Space Grotesk', 'Noto Sans TC', sans-serif;
  font-size: 3rem;
  font-weight: 800;
  line-height: 1.15;
  margin: 0 0 20px 0;
  letter-spacing: -0.02em;
}

.slide-default :deep(p) {
  color: var(--text-body, #475569);
  font-family: 'Manrope', 'Noto Sans TC', sans-serif;
  font-size: 1.1rem;
  line-height: 1.5;
}
</style>
