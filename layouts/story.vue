<!--
  故事/內容頁 — 白底，左文右圖 icon
  用法：
  ---
  layout: story
  label: 第一次低潮
  icon: 🏪  （選填，或用 public/brand/ 下的 SVG）
  ---
  # 退伍，開了一家化妝品店

  - 退伍金 30 萬 → 開店 → 不到兩年失敗
  - 刷信用卡進貨 + 買房 → 欠債 3-400 萬
-->
<template>
  <div class="story-layout">
    <div class="story-left">
      <p v-if="$slidev.frontmatter.label" class="story-label">{{ $slidev.frontmatter.label }}</p>
      <slot />
    </div>
    <div v-if="$slidev.frontmatter.icon" class="story-right">
      <span class="story-icon">{{ $slidev.frontmatter.icon }}</span>
    </div>
  </div>
</template>

<style scoped>
.story-layout {
  width: 100%;
  height: 100%;
  background: var(--bg-light, #fafafa);
  display: flex;
  align-items: center;
  padding: 60px 80px;
  gap: 40px;
}

.story-left {
  flex: 1;
}

.story-right {
  flex: 0 0 auto;
  display: flex;
  align-items: center;
  justify-content: center;
}

.story-icon {
  font-size: 10rem;
  opacity: 0.15;
}

.story-label {
  color: var(--brand-purple, #7c3aed);
  font-size: 0.85rem;
  font-weight: 700;
  letter-spacing: 0.05em;
  margin-bottom: 8px;
}

.story-layout :deep(h1) {
  color: var(--text-dark, #1a1a1a);
  font-size: 2.5rem;
  font-weight: 900;
  margin: 0 0 20px 0;
  line-height: 1.3;
}

.story-layout :deep(ul) {
  list-style: none;
  padding: 0;
  margin: 0;
}

.story-layout :deep(li) {
  color: #4b5563;
  font-size: 1.1rem;
  line-height: 1.8;
  padding-left: 0;
}

.story-layout :deep(p) {
  color: #4b5563;
  font-size: 1.1rem;
  line-height: 1.8;
}

.story-layout :deep(.cta-text) {
  color: var(--brand-orange, #ea580c);
  font-weight: 600;
}
</style>
