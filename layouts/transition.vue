<!--
  紫色轉場頁 — 紫色底，白字，播放圖示裝飾
  用法：
  ---
  layout: transition
  ---
  # 說了很多，接下來直接做給你看
-->
<template>
  <div class="transition-layout">
    <div class="transition-content">
      <slot />
    </div>
    <div class="transition-deco" aria-hidden="true">
      <svg viewBox="0 0 80 80" fill="none" xmlns="http://www.w3.org/2000/svg">
        <circle cx="40" cy="40" r="38" stroke="rgba(255,255,255,0.2)" stroke-width="2"/>
        <path d="M32 24L58 40L32 56V24Z" fill="rgba(255,255,255,0.25)"/>
      </svg>
    </div>
    <div class="transition-circle-1" aria-hidden="true"></div>
    <div class="transition-circle-2" aria-hidden="true"></div>
  </div>
</template>

<style scoped>
.transition-layout {
  width: 100%;
  height: 100%;
  background: var(--bg-purple, #7c3aed);
  display: flex;
  align-items: center;
  padding: 60px 100px;
  position: relative;
  overflow: hidden;
}

.transition-content {
  position: relative;
  z-index: 1;
  max-width: 65%;
}

.transition-content :deep(h1) {
  color: white;
  font-size: 3rem;
  font-weight: 900;
  line-height: 1.4;
  margin: 0;
}

.transition-content :deep(p) {
  color: rgba(255, 255, 255, 0.7);
  font-size: 1.1rem;
  margin-top: 20px;
}

.transition-deco {
  position: absolute;
  right: 80px;
  top: 50%;
  transform: translateY(-50%);
  width: 160px;
  height: 160px;
  z-index: 0;
}

.transition-circle-1 {
  position: absolute;
  top: 30px;
  left: 60px;
  width: 30px;
  height: 30px;
  border-radius: 50%;
  background: rgba(255, 255, 255, 0.1);
}

.transition-circle-2 {
  position: absolute;
  bottom: 50px;
  right: 200px;
  width: 18px;
  height: 18px;
  border-radius: 50%;
  background: rgba(255, 255, 255, 0.08);
}
</style>
