<!--
  藍色課程頁 — 藍底，白字，課程相關
  用法：
  ---
  layout: course
  ---
  # 內容
-->
<template>
  <div class="course-layout">
    <div class="course-content">
      <slot />
    </div>
    <div class="course-circle-1" aria-hidden="true"></div>
    <div class="course-circle-2" aria-hidden="true"></div>
  </div>
</template>

<style scoped>
.course-layout {
  width: 100%;
  height: 100%;
  background: var(--bg-blue, #1a5276);
  display: flex;
  align-items: center;
  padding: 60px 80px;
  position: relative;
  overflow: hidden;
}

.course-content {
  position: relative;
  z-index: 1;
  width: 100%;
}

.course-content :deep(h1) {
  color: white;
  font-size: 2.8rem;
  font-weight: 900;
  line-height: 1.4;
  margin: 0 0 20px 0;
}

.course-content :deep(p) {
  color: rgba(255, 255, 255, 0.7);
  font-size: 1.05rem;
  line-height: 1.8;
}

.course-circle-1 {
  position: absolute;
  top: -30px;
  right: 100px;
  width: 100px;
  height: 100px;
  border-radius: 50%;
  background: rgba(255, 255, 255, 0.06);
}

.course-circle-2 {
  position: absolute;
  bottom: 30px;
  right: 40px;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background: rgba(255, 255, 255, 0.04);
}
</style>
