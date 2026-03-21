<!--
  階段轉場頁 — 深藍底，階段編號 + 轉換方向
  用法：
  ---
  layout: stage
  stage: 2
  from: 觀望
  to: 開放
  subtitle: 三段失敗故事
  note: 「你憑什麼？」→「你跟我一樣」
  ---
-->
<template>
  <div class="stage-layout deco-circles-dark">
    <div class="stage-content">
      <p class="stage-badge">階段 {{ $slidev.frontmatter.stage }}</p>
      <h1 class="stage-title">{{ $slidev.frontmatter.from }} → {{ $slidev.frontmatter.to }}</h1>
      <p v-if="$slidev.frontmatter.subtitle" class="stage-subtitle">{{ $slidev.frontmatter.subtitle }}</p>
      <p v-if="$slidev.frontmatter.note" class="stage-note">{{ $slidev.frontmatter.note }}</p>
      <slot />
    </div>
  </div>
</template>

<style scoped>
.stage-layout {
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

.stage-content {
  position: relative;
  z-index: 1;
}

.stage-badge {
  display: inline-block;
  background: var(--brand-purple, #7c3aed);
  color: white;
  padding: 6px 24px;
  border-radius: 24px;
  font-size: 0.85rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  margin-bottom: 24px;
}

.stage-title {
  color: white;
  font-size: 4rem;
  font-weight: 900;
  margin: 0;
  line-height: 1.2;
}

.stage-subtitle {
  color: rgba(255, 255, 255, 0.55);
  font-size: 1.15rem;
  margin-top: 20px;
}

.stage-note {
  color: var(--brand-orange, #ea580c);
  font-size: 0.9rem;
  margin-top: 16px;
  opacity: 0.85;
}
</style>
