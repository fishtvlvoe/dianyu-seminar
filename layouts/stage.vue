<!--
  階段轉場頁 — 白底 + 置中
-->
<template>
  <div class="slide-stage">
    <div class="top-bar"></div>
    <div class="stage-content">
      <div class="stage-line"></div>
      <p class="stage-label">階段 {{ $slidev.frontmatter.stage }}</p>
      <h1 class="stage-title">{{ $slidev.frontmatter.from }} → {{ $slidev.frontmatter.to }}</h1>
      <p v-if="$slidev.frontmatter.subtitle" class="stage-sub">{{ $slidev.frontmatter.subtitle }}</p>
      <div class="stage-line"></div>
      <slot />
    </div>
  </div>
</template>

<style scoped>
.slide-stage {
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

.stage-line {
  width: 200px;
  height: 2px;
  background: #E2E8F0;
  margin: 0 auto 24px;
}

.stage-label {
  font-family: 'Space Mono', monospace;
  color: #0369A1;
  font-size: 1rem;
  margin-bottom: 12px;
}

.stage-title {
  color: #0F172A;
  font-family: 'Space Grotesk', 'Noto Sans TC', sans-serif;
  font-size: 4.5rem;
  font-weight: 800;
  line-height: 1.1;
  letter-spacing: -2px;
  margin: 0 0 20px;
}

.stage-sub {
  color: #64748B;
  font-family: 'Manrope', 'Noto Sans TC', sans-serif;
  font-size: 1.05rem;
  margin-bottom: 24px;
}
</style>
