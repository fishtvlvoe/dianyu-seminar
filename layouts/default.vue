<!--
  預設白底內容頁 — 左上裝飾圓圈 + 右側可選裝飾圖示
  用法：直接寫內容，不需指定 layout
-->
<template>
  <div class="default-layout deco-circles">
    <div class="default-content">
      <slot />
    </div>
  </div>
</template>

<style scoped>
.default-layout {
  width: 100%;
  height: 100%;
  background: var(--bg-light, #fafafa);
  padding: var(--slide-padding, 60px 80px);
  position: relative;
  overflow: hidden;
}

.default-content {
  position: relative;
  z-index: 1;
  height: 100%;
}

.default-content :deep(h1) {
  color: var(--text-dark, #1a1a1a);
  font-size: 2.8rem;
  font-weight: 900;
  margin: 0 0 20px 0;
  line-height: 1.3;
}

.default-content :deep(h2) {
  color: var(--text-dark, #1a1a1a);
  font-size: 1.8rem;
  font-weight: 900;
  margin: 0 0 16px 0;
}

.default-content :deep(p) {
  color: var(--text-body, #4b5563);
  font-size: 1.05rem;
  line-height: 1.8;
}

.default-content :deep(ul) {
  list-style: none;
  padding: 0;
  margin: 0;
}

.default-content :deep(li) {
  color: var(--text-body, #4b5563);
  font-size: 1.05rem;
  line-height: 2;
  padding-left: 0;
}

.default-content :deep(li::before) {
  content: '→ ';
  color: var(--brand-purple, #7c3aed);
  font-weight: 700;
  margin-right: 4px;
}
</style>
