<!--
  金句頁 — 深藍底，大字金句置中
  用法：
  ---
  layout: quote
  ---
  # 真正讓人崩潰的，不是忙。是忙了沒有結果。
-->
<template>
  <div class="quote-layout">
    <div class="quote-content">
      <slot />
    </div>
  </div>
</template>

<style scoped>
.quote-layout {
  width: 100%;
  height: 100%;
  background: var(--bg-dark, #1a1745);
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 60px 120px;
}

.quote-content :deep(h1) {
  color: white;
  font-size: 3rem;
  font-weight: 900;
  line-height: 1.4;
}

.quote-content :deep(p) {
  color: rgba(255, 255, 255, 0.5);
  font-size: 1.1rem;
  margin-top: 24px;
}
</style>
