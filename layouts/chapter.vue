<!--
  章節轉場頁 — 白底 + 置中大字 + 藍色裝飾
-->
<template>
  <div class="slide-chapter">
    <div class="top-bar"></div>
    <div class="chapter-content">
      <div class="chapter-line"></div>
      <p class="chapter-label">{{ $slidev.frontmatter.label || '第' + $slidev.frontmatter.chapter + '幕' }}</p>
      <h1 class="chapter-title">{{ $slidev.frontmatter.title }}</h1>
      <p v-if="$slidev.frontmatter.subtitle" class="chapter-sub">{{ $slidev.frontmatter.subtitle }}</p>
      <div class="chapter-line"></div>
      <slot />
    </div>
  </div>
</template>

<style scoped>
.slide-chapter {
  width: 100%;
  height: 100%;
  background: #FAFAFA !important;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  position: relative;
}

.top-bar {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 4px;
  background: #0369A1;
}

.chapter-line {
  width: 200px;
  height: 2px;
  background: #E2E8F0;
  margin: 0 auto 24px;
}

.chapter-label {
  font-family: 'Space Mono', monospace;
  color: #0369A1;
  font-size: 1rem;
  margin-bottom: 16px;
}

.chapter-title {
  color: #0F172A;
  font-family: 'Space Grotesk', 'Noto Sans TC', sans-serif;
  font-size: 4.5rem;
  font-weight: 800;
  line-height: 1.1;
  letter-spacing: -2px;
  margin: 0;
}

.chapter-sub {
  color: #64748B;
  font-family: 'Manrope', 'Noto Sans TC', sans-serif;
  font-size: 1.05rem;
  margin-top: 20px;
  margin-bottom: 24px;
}
</style>
