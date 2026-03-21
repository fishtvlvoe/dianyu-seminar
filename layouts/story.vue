<!--
  故事/概念頁 — 白底 + 頂部藍條 + 左文右視覺區
  對應 Pencil: D - Concept + Visual
-->
<template>
  <div class="slide-story">
    <div class="top-bar"></div>
    <div class="story-left">
      <p v-if="$slidev.frontmatter.label" class="story-label">{{ $slidev.frontmatter.label }}</p>
      <slot />
      <div v-if="$slidev.frontmatter.num" class="slide-num">{{ $slidev.frontmatter.num }}</div>
    </div>
    <div v-if="$slidev.frontmatter.visual !== false" class="story-right">
      <div class="visual-area">
        <span class="visual-area-label">{{ $slidev.frontmatter.visualLabel || '圖解區域' }}</span>
      </div>
    </div>
  </div>
</template>

<style scoped>
.slide-story {
  width: 100%;
  height: 100%;
  background: var(--bg-light, #FAFAFA);
  display: flex;
  position: relative;
  overflow: hidden;
}

.story-left {
  flex: 1;
  padding: 80px 60px 80px 100px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  position: relative;
}

.story-label {
  font-family: var(--font-mono, 'Space Mono');
  color: var(--brand, #0369A1);
  font-size: 0.85rem;
  margin-bottom: 16px;
}

.story-right {
  flex: 0 0 420px;
  padding: 80px 60px 80px 0;
  display: flex;
  align-items: center;
}

.story-left :deep(h1) {
  color: var(--text-heading, #0F172A);
  font-size: 3rem;
  font-weight: 800;
  line-height: 1.15;
  margin: 0 0 24px 0;
  letter-spacing: -0.02em;
}

.story-left :deep(p) {
  color: var(--text-body, #475569);
  font-size: 1.05rem;
  line-height: 1.6;
}

.story-left :deep(ul) {
  list-style: none;
  padding: 0;
}

.story-left :deep(li) {
  color: var(--text-body, #475569);
  font-size: 1.05rem;
  line-height: 1.8;
}

.visual-area {
  width: 100%;
  height: 80%;
  background: var(--border, #E2E8F0);
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.visual-area-label {
  color: var(--text-faint, #94A3B8);
  font-size: 1rem;
  font-weight: 500;
}
</style>
