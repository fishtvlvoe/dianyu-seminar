<!--
  故事/內容頁 — 白底 + 左文 + 右側大型半透明圖示
  用法：
  ---
  layout: story
  label: 第一次低潮
  icon: 🏪
  ---
-->
<template>
  <div class="story-layout deco-circles">
    <div class="story-content">
      <p v-if="$slidev.frontmatter.label" class="story-label">{{ $slidev.frontmatter.label }}</p>
      <slot />
    </div>
    <div v-if="$slidev.frontmatter.icon" class="story-deco-icon" aria-hidden="true">
      {{ $slidev.frontmatter.icon }}
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
  position: relative;
  overflow: hidden;
}

.story-content {
  flex: 1;
  max-width: 60%;
  position: relative;
  z-index: 1;
}

.story-label {
  color: var(--brand-purple, #7c3aed);
  font-size: 0.85rem;
  font-weight: 700;
  letter-spacing: 0.05em;
  margin-bottom: 12px;
}

.story-deco-icon {
  position: absolute;
  right: 40px;
  top: 50%;
  transform: translateY(-50%);
  font-size: 14rem;
  opacity: 0.07;
  z-index: 0;
  line-height: 1;
  pointer-events: none;
}

.story-layout :deep(h1) {
  color: var(--text-dark, #1a1a1a);
  font-size: 2.8rem;
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
  color: var(--text-body, #4b5563);
  font-size: 1.05rem;
  line-height: 2;
}

.story-layout :deep(li::before) {
  content: '→ ';
  color: var(--brand-purple, #7c3aed);
  font-weight: 700;
  margin-right: 4px;
}

.story-layout :deep(p) {
  color: var(--text-body, #4b5563);
  font-size: 1.05rem;
  line-height: 1.8;
}
</style>
