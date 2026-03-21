<!--
  章節頁 — 深藍底，大標題置中，裝飾圓圈
  用法：
  ---
  layout: chapter
  chapter: 1
  title: 三段人生故事
  subtitle: 從 20 幾歲到 48 歲的迴圈
  ---
-->
<template>
  <div class="chapter-layout deco-circles-dark">
    <div class="chapter-content">
      <p class="chapter-label">
        {{ $slidev.frontmatter.label || '第' + $slidev.frontmatter.chapter + '幕' }} · CHAPTER {{ $slidev.frontmatter.chapter }}
      </p>
      <h1 class="chapter-title">{{ $slidev.frontmatter.title }}</h1>
      <p v-if="$slidev.frontmatter.subtitle" class="chapter-subtitle">{{ $slidev.frontmatter.subtitle }}</p>
      <slot />
    </div>
  </div>
</template>

<style scoped>
.chapter-layout {
  width: 100%;
  height: 100%;
  background: var(--bg-dark, #13112b);
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.chapter-content {
  position: relative;
  z-index: 1;
  max-width: 80%;
}

.chapter-label {
  color: var(--brand-purple-light, #a78bfa);
  font-size: 0.9rem;
  font-weight: 600;
  letter-spacing: 0.15em;
  margin-bottom: 20px;
}

.chapter-title {
  color: white;
  font-size: 4rem;
  font-weight: 900;
  margin: 0;
  line-height: 1.2;
}

.chapter-subtitle {
  color: rgba(255, 255, 255, 0.45);
  font-size: 1.1rem;
  margin-top: 20px;
}
</style>
