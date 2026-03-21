<!--
  章節轉場頁 — 深色底，置中大字
  對應 Pencil: B - Section Break
-->
<template>
  <div class="slide-chapter">
    <div class="chapter-content">
      <div class="chapter-line-top"></div>
      <p class="chapter-label">{{ $slidev.frontmatter.label || '第' + $slidev.frontmatter.chapter + '幕' }}</p>
      <h1 class="chapter-title">{{ $slidev.frontmatter.title }}</h1>
      <p v-if="$slidev.frontmatter.subtitle" class="chapter-sub">{{ $slidev.frontmatter.subtitle }}</p>
      <div class="chapter-line-bot"></div>
      <p v-if="$slidev.frontmatter.emotion" class="chapter-emotion">{{ $slidev.frontmatter.emotion }}</p>
      <slot />
    </div>
  </div>
</template>

<style scoped>
.slide-chapter {
  width: 100%;
  height: 100%;
  background: var(--bg-dark, #0F172A);
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.chapter-content {
  max-width: 70%;
}

.chapter-line-top,
.chapter-line-bot {
  width: 200px;
  height: 2px;
  background: #334155;
  margin: 0 auto;
}

.chapter-line-top {
  margin-bottom: 24px;
}

.chapter-line-bot {
  margin-top: 32px;
}

.chapter-label {
  font-family: var(--font-mono, 'Space Mono');
  color: var(--brand, #0369A1);
  font-size: 1rem;
  margin-bottom: 16px;
}

.chapter-title {
  color: #FAFAFA;
  font-size: 5rem;
  font-weight: 800;
  line-height: 1.1;
  letter-spacing: -2px;
  margin: 0;
}

.chapter-sub {
  color: var(--text-muted, #64748B);
  font-size: 1rem;
  margin-top: 20px;
}

.chapter-emotion {
  color: var(--text-body, #475569);
  font-size: 0.9rem;
  margin-top: 20px;
}
</style>
