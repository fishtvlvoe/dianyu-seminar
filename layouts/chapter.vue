<!--
  章節頁 — 深藍底，大標題置中
  用法：
  ---
  layout: chapter
  chapter: 1
  title: 三段人生故事
  subtitle: 從 20 幾歲到 48 歲的迴圈
  ---
-->
<template>
  <div class="chapter-layout">
    <div class="chapter-content">
      <div class="divider"></div>
      <p class="chapter-label">
        {{ $slidev.frontmatter.label || '第' + $slidev.frontmatter.chapter + '幕' }} · CHAPTER {{ $slidev.frontmatter.chapter }}
      </p>
      <h1 class="chapter-title">{{ $slidev.frontmatter.title }}</h1>
      <p v-if="$slidev.frontmatter.subtitle" class="chapter-subtitle">{{ $slidev.frontmatter.subtitle }}</p>
      <div class="divider"></div>
      <slot />
    </div>
  </div>
</template>

<style scoped>
.chapter-layout {
  width: 100%;
  height: 100%;
  background: var(--bg-dark, #1a1745);
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.divider {
  width: 80px;
  height: 3px;
  background: var(--brand-purple, #7c3aed);
  margin: 20px auto;
  border-radius: 2px;
}

.chapter-label {
  color: var(--brand-purple, #7c3aed);
  font-size: 0.95rem;
  font-weight: 600;
  letter-spacing: 0.15em;
  margin-bottom: 16px;
}

.chapter-title {
  color: white;
  font-size: 4.5rem;
  font-weight: 900;
  margin: 0;
  line-height: 1.1;
}

.chapter-subtitle {
  color: rgba(255, 255, 255, 0.5);
  font-size: 1.1rem;
  margin-top: 20px;
}
</style>
