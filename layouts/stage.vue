<!--
  階段轉場頁 — 深色底 + 置中
  對應 Pencil: B - Section Break 的變體
-->
<template>
  <div class="slide-stage">
    <div class="stage-content">
      <div class="stage-line"></div>
      <p class="stage-label">階段 {{ $slidev.frontmatter.stage }}</p>
      <h1 class="stage-title">{{ $slidev.frontmatter.from }} → {{ $slidev.frontmatter.to }}</h1>
      <p v-if="$slidev.frontmatter.subtitle" class="stage-sub">{{ $slidev.frontmatter.subtitle }}</p>
      <div class="stage-line"></div>
      <p v-if="$slidev.frontmatter.note" class="stage-note">{{ $slidev.frontmatter.note }}</p>
      <slot />
    </div>
  </div>
</template>

<style scoped>
.slide-stage {
  width: 100%;
  height: 100%;
  background: var(--bg-dark, #0F172A);
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.stage-content {
  max-width: 70%;
}

.stage-line {
  width: 200px;
  height: 2px;
  background: #334155;
  margin: 0 auto 24px;
}

.stage-label {
  font-family: var(--font-mono, 'Space Mono');
  color: var(--brand, #0369A1);
  font-size: 1rem;
  margin-bottom: 12px;
}

.stage-title {
  color: #FAFAFA;
  font-size: 5rem;
  font-weight: 800;
  line-height: 1.1;
  letter-spacing: -2px;
  margin: 0 0 20px;
}

.stage-sub {
  color: var(--text-muted, #64748B);
  font-size: 1.05rem;
  margin-bottom: 24px;
}

.stage-note {
  color: var(--text-body, #475569);
  font-size: 0.9rem;
  margin-top: 16px;
}
</style>
