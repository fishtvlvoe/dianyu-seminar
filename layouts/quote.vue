<!--
  金句頁 — 深藍底，大字金句，右側可選裝飾圖示
  用法：
  ---
  layout: quote
  icon: 💎（選填）
  ---
  # 金句內容
-->
<template>
  <div class="quote-layout deco-circles-dark">
    <div class="quote-content">
      <slot />
    </div>
    <div v-if="$slidev.frontmatter.icon" class="quote-deco-icon" aria-hidden="true">
      {{ $slidev.frontmatter.icon }}
    </div>
  </div>
</template>

<style scoped>
.quote-layout {
  width: 100%;
  height: 100%;
  background: var(--bg-dark, #13112b);
  display: flex;
  align-items: center;
  padding: 60px 100px;
  position: relative;
  overflow: hidden;
}

.quote-content {
  position: relative;
  z-index: 1;
  max-width: 70%;
}

.quote-content :deep(h1) {
  color: white;
  font-size: 2.8rem;
  font-weight: 900;
  line-height: 1.5;
  margin: 0;
}

.quote-content :deep(p) {
  color: rgba(255, 255, 255, 0.45);
  font-size: 1.1rem;
  margin-top: 24px;
  line-height: 1.8;
}

.quote-deco-icon {
  position: absolute;
  right: 60px;
  top: 50%;
  transform: translateY(-50%);
  font-size: 14rem;
  opacity: 0.06;
  z-index: 0;
  line-height: 1;
  pointer-events: none;
}
</style>
