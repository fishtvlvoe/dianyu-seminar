<!--
  深色轉場頁 — 深藍底 + 白字（報價/課程頁面共用）
  對應 Pencil: I - Demo Screenshot 的深色風格
-->
<template>
  <div class="slide-transition">
    <div class="top-bar" style="background: var(--brand);"></div>
    <div class="transition-content">
      <slot />
    </div>
  </div>
</template>

<style scoped>
.slide-transition {
  width: 100%;
  height: 100%;
  background: var(--bg-dark, #0F172A);
  position: relative;
  overflow: hidden;
}

.transition-content {
  position: relative;
  z-index: 1;
  padding: 80px 100px;
  height: 100%;
}

.transition-content :deep(h1) {
  color: #FAFAFA;
  font-size: 3rem;
  font-weight: 800;
  line-height: 1.2;
  margin: 0 0 20px 0;
}

.transition-content :deep(p) {
  color: rgba(255, 255, 255, 0.65);
  font-size: 1.05rem;
  line-height: 1.6;
}

.transition-content :deep(ul) {
  list-style: none;
  padding: 0;
}

.transition-content :deep(li) {
  color: rgba(255, 255, 255, 0.65);
  font-size: 1.05rem;
  line-height: 1.8;
}
</style>
