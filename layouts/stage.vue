<!--
  階段轉場頁 — 深藍底，置中
  用法：
  ---
  layout: stage
  stage: 1
  from: 防備
  to: 觀望
  subtitle: 開場：拉椅子 + 檢查表
  note: 「又一個賣課的吧」→「那就聽聽看」
  ---
-->
<template>
  <div class="stage-layout">
    <div class="stage-content">
      <p class="stage-label">階段 ⓪</p>
      <h1 class="stage-title">{{ $slidev.frontmatter.from }} → {{ $slidev.frontmatter.to }}</h1>
      <p v-if="$slidev.frontmatter.subtitle" class="stage-subtitle">{{ $slidev.frontmatter.subtitle }}</p>
      <p v-if="$slidev.frontmatter.note" class="stage-note">{{ $slidev.frontmatter.note }}</p>
    </div>
  </div>
</template>

<script setup>
const props = defineProps()
</script>

<style scoped>
.stage-layout {
  width: 100%;
  height: 100%;
  background: var(--bg-dark, #1a1745);
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.stage-label {
  color: var(--brand-purple, #7c3aed);
  font-size: 1rem;
  font-weight: 600;
  letter-spacing: 0.1em;
  margin-bottom: 12px;
}

.stage-title {
  color: white;
  font-size: 3.5rem;
  font-weight: 900;
  margin: 0;
  line-height: 1.2;
}

.stage-subtitle {
  color: rgba(255, 255, 255, 0.6);
  font-size: 1.1rem;
  margin-top: 16px;
}

.stage-note {
  color: var(--brand-orange, #ea580c);
  font-size: 0.9rem;
  margin-top: 12px;
  opacity: 0.8;
}
</style>
