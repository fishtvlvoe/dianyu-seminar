---
theme: none
title: 電馭工作流 — 線上說明會
highlighter: shiki
lineNumbers: false
drawings:
  persist: false
transition: fade
mdc: true
---

<style>
@import './styles/index.css';
</style>

<!-- S01 封面 ── 白底，置中大標 -->
<div class="deco-circles w-full h-full flex flex-col items-center justify-center text-center" style="background:#fafafa; padding: 60px 80px; position:relative; overflow:hidden;">
  <div style="position:relative; z-index:1;">
<span class="label label-purple" style="letter-spacing:0.08em;">線上說明會</span>
<h1 style="font-size:5.5rem; font-weight:900; color:#1a1a1a; margin:28px 0 16px; line-height:1.1; letter-spacing:-0.01em;">電馭工作流</h1>
<p style="font-size:1.3rem; color:#6b7280; margin:0 0 48px;">這不是教工具，而是把生活節奏拿回來</p>
<p style="font-size:1rem; color:#9ca3af; font-weight:500;">老魚（余啓彰）</p>
  </div>
</div>

<!--
開場白，確認音訊、畫面正常。歡迎大家。
-->

---

<!-- S02 拉椅子 + 預告結構 ── 白底，左文，右側裝飾圖示 -->
<div class="deco-circles w-full h-full" style="background:#fafafa; padding:60px 80px; position:relative; overflow:hidden;">
  <div class="deco-icon">🎁</div>
  <div style="position:relative; z-index:1; max-width:58%;">
<span class="label label-purple" style="margin-bottom:20px; display:inline-block;">開場</span>
<h1 style="font-size:2.8rem; font-weight:900; color:#1a1a1a; margin:0 0 32px; line-height:1.3;">今天你會帶走<br />四個東西</h1>

<v-clicks>

<div class="flex flex-col gap-3">
<div class="flex items-center gap-4">
<span style="width:32px;height:32px;border-radius:50%;background:#7c3aed;color:white;font-size:0.85rem;font-weight:900;display:flex;align-items:center;justify-content:center;flex-shrink:0;">1</span>
<span style="font-size:1.05rem;color:#374151;font-weight:500;">檢測你工作卡在哪的方法</span>
</div>
<div class="flex items-center gap-4">
<span style="width:32px;height:32px;border-radius:50%;background:#7c3aed;color:white;font-size:0.85rem;font-weight:900;display:flex;align-items:center;justify-content:center;flex-shrink:0;">2</span>
<span style="font-size:1.05rem;color:#374151;font-weight:500;">讓 AI 聽懂你說話的提問框架</span>
</div>
<div class="flex items-center gap-4">
<span style="width:32px;height:32px;border-radius:50%;background:#7c3aed;color:white;font-size:0.85rem;font-weight:900;display:flex;align-items:center;justify-content:center;flex-shrink:0;">3</span>
<span style="font-size:1.05rem;color:#374151;font-weight:500;">你今天就能帶走的工作流模板</span>
</div>
<div class="flex items-center gap-4">
<span style="width:32px;height:32px;border-radius:50%;background:#7c3aed;color:white;font-size:0.85rem;font-weight:900;display:flex;align-items:center;justify-content:center;flex-shrink:0;">4</span>
<span style="font-size:1.05rem;color:#374151;font-weight:500;">屬於你自己的行動計畫</span>
</div>
</div>

</v-clicks>

<div v-click style="margin-top:28px; padding:16px 24px; background:#fff7ed; border-left:4px solid #ea580c; border-radius:0 12px 12px 0;">
<p style="margin:0; color:#ea580c; font-weight:700; font-size:1rem;">不管有沒有報名，前三個今天就是你的</p>
</div>

  </div>
</div>

<!--
「各位同學好，我是老魚。我都會叫大家同學，因為我們都是在學習的人——你會是我的老師，我也會是你的老師。」
-->

---

<!-- S03 自介：教學平台 ── 白底，截圖展示 -->
<div class="deco-circles w-full h-full" style="background:#fafafa; padding:60px 80px; position:relative; overflow:hidden;">
  <div style="position:relative; z-index:1;">
<span class="label label-purple" style="margin-bottom:20px; display:inline-block;">自我介紹</span>
<h1 style="font-size:2.4rem; font-weight:900; color:#1a1a1a; margin:0 0 32px;">教學平台</h1>

<!-- 模擬課程平台 UI -->
<div style="background:white; border:1px solid #e5e7eb; border-radius:16px; overflow:hidden; box-shadow:0 4px 20px rgba(0,0,0,0.06);">
  <!-- 平台導覽列 -->
  <div style="background:#f9fafb; border-bottom:1px solid #e5e7eb; padding:12px 20px; display:flex; align-items:center; gap:16px;">
    <span style="font-size:0.8rem; color:#6b7280; font-weight:600;">課程 (14)</span>
    <div style="display:flex; gap:8px; margin-left:auto;">
      <span style="font-size:0.75rem; background:#7c3aed; color:white; padding:4px 12px; border-radius:6px; font-weight:600;">所有課程</span>
      <span style="font-size:0.75rem; color:#6b7280; padding:4px 12px;">我的課</span>
    </div>
  </div>
  <!-- 課程卡片列 -->
  <div style="padding:20px; display:grid; grid-template-columns:1fr 1fr 1fr; gap:16px;">
    <div style="border-radius:12px; overflow:hidden; border:1px solid #e5e7eb;">
      <div style="height:80px; background:linear-gradient(135deg,#6366f1,#7c3aed); display:flex; align-items:center; justify-content:center;">
        <span style="font-size:1.5rem;">💬</span>
      </div>
      <div style="padding:12px;">
        <p style="font-size:0.8rem; font-weight:700; color:#1a1a1a; margin:0 0 4px;">1 - 直接聊聊</p>
        <p style="font-size:0.7rem; color:#9ca3af; margin:0;">2 堂課｜96% 完成</p>
      </div>
    </div>
    <div style="border-radius:12px; overflow:hidden; border:1px solid #e5e7eb;">
      <div style="height:80px; background:linear-gradient(135deg,#0ea5e9,#2563eb); display:flex; align-items:center; justify-content:center;">
        <span style="font-size:1.5rem;">🏠</span>
      </div>
      <div style="padding:12px;">
        <p style="font-size:0.8rem; font-weight:700; color:#1a1a1a; margin:0 0 4px;">2 - 私域社群功能</p>
        <p style="font-size:0.7rem; color:#9ca3af; margin:0;">4 堂課｜98% 完成</p>
      </div>
    </div>
    <div style="border-radius:12px; overflow:hidden; border:1px solid #e5e7eb;">
      <div style="height:80px; background:linear-gradient(135deg,#10b981,#059669); display:flex; align-items:center; justify-content:center;">
        <span style="font-size:1.5rem;">⚙️</span>
      </div>
      <div style="padding:12px;">
        <p style="font-size:0.8rem; font-weight:700; color:#1a1a1a; margin:0 0 4px;">3 - 自動化社群管理者</p>
        <p style="font-size:0.7rem; color:#9ca3af; margin:0;">8 堂課｜0% 完成</p>
      </div>
    </div>
  </div>
</div>
  </div>
</div>

<!--
教學平台目前有 14 堂課，帶過超過 3,000 個學員。
-->

---
layout: story
label: 自我介紹
icon: 🐟
---

# Fish / 老魚

<v-clicks>

- 網路行銷教學 **15 年**
- 出版《第一次當網紅就上手》
- YouTuber / 線上教練
- 現在：台南，一人公司

</v-clicks>

<!--
快速自我介紹，不拖太久。重點是建立「我也是普通人，跌跌撞撞走過來的」印象。
-->

---

<!-- S05 引導打 1 ── 白底，置中大字 CTA -->
<div class="deco-circles w-full h-full flex flex-col items-center justify-center text-center" style="background:#fafafa; padding:60px 80px; position:relative; overflow:hidden;">
  <div class="deco-icon" style="font-size:14rem; right:40px;">🙋</div>
  <div style="position:relative; z-index:1; max-width:680px;">
<h1 style="font-size:3rem; font-weight:900; color:#1a1a1a; margin:0 0 24px; line-height:1.35;">你覺得 AI 可以幫助你嗎？</h1>
<p style="font-size:1.15rem; color:#4b5563; margin:0 0 40px; line-height:1.8;">如果你覺得 AI 可以協助你的工作、<br />讓生活變得更簡單</p>
<div style="display:inline-flex; align-items:center; gap:16px; background:#7c3aed; color:white; padding:20px 48px; border-radius:16px; font-size:1.4rem; font-weight:900;">
  <span>幫我打個</span>
  <span style="font-size:2.5rem;">1</span>
</div>
  </div>
</div>

<!--
確認大家今天過來的目的，建立共識。等留言出現 1 才繼續往下。
-->

---

<!-- S06 QR Code 檢查表 ── 白底，左文右 QR -->
<div class="deco-circles w-full h-full" style="background:#fafafa; padding:60px 80px; position:relative; overflow:hidden;">
  <div style="position:relative; z-index:1; display:grid; grid-template-columns:1fr 1fr; gap:48px; align-items:center; height:100%;">
<div>
  <span class="label label-purple" style="margin-bottom:20px; display:inline-block;">送你一份禮物</span>
  <h1 style="font-size:2.8rem; font-weight:900; color:#1a1a1a; margin:0 0 24px; line-height:1.3;">掃碼做測驗</h1>
  <div class="flex flex-col gap-4">
    <div style="display:flex; align-items:flex-start; gap:12px;">
      <span style="width:28px; height:28px; border-radius:50%; background:rgba(124,58,237,0.1); color:#7c3aed; font-size:0.8rem; font-weight:900; display:flex; align-items:center; justify-content:center; flex-shrink:0; margin-top:2px;">12</span>
      <div>
        <p style="font-size:0.95rem; font-weight:700; color:#1a1a1a; margin:0 0 2px;">12 題，分三類</p>
        <p style="font-size:0.85rem; color:#6b7280; margin:0;">收集｜整理｜決策</p>
      </div>
    </div>
    <div style="display:flex; align-items:flex-start; gap:12px;">
      <span style="width:28px; height:28px; border-radius:50%; background:rgba(124,58,237,0.1); color:#7c3aed; font-size:1rem; display:flex; align-items:center; justify-content:center; flex-shrink:0; margin-top:2px;">📋</span>
      <div>
        <p style="font-size:0.95rem; font-weight:700; color:#1a1a1a; margin:0 0 2px;">每頁 4 題，勾完自動算分</p>
        <p style="font-size:0.85rem; color:#6b7280; margin:0;">大概 30 秒就做完了</p>
      </div>
    </div>
  </div>
  <div style="margin-top:28px; padding:14px 20px; background:#fff7ed; border-left:4px solid #ea580c; border-radius:0 12px 12px 0;">
    <p style="margin:0; color:#ea580c; font-weight:700; font-size:0.95rem;">做完的人把分數打在留言區</p>
  </div>
</div>
<!-- QR Code 佔位 -->
<div style="display:flex; flex-direction:column; align-items:center; gap:16px;">
  <div style="width:200px; height:200px; border-radius:16px; border:2px solid #e5e7eb; background:white; display:flex; align-items:center; justify-content:center; box-shadow:0 4px 20px rgba(0,0,0,0.06);">
    <span style="color:#d1d5db; font-size:0.8rem; text-align:center;">QR Code<br />檢查表</span>
  </div>
  <p style="font-size:0.8rem; color:#9ca3af; text-align:center;">留言區也有連結</p>
</div>
  </div>
</div>

<!--
「螢幕上有一個 QR Code，掃一下。用電腦的人，留言區也有連結。」
做完之後請把你的分數打在留言區讓我知道。
-->

---

<!-- S07 分數解讀 ── 白底，三色分數卡片 -->
<div class="deco-circles w-full h-full" style="background:#fafafa; padding:60px 80px; position:relative; overflow:hidden;">
  <div class="deco-icon" style="font-size:12rem;">📊</div>
  <div style="position:relative; z-index:1; max-width:62%;">
<h1 style="font-size:2.8rem; font-weight:900; color:#1a1a1a; margin:0 0 32px;">你的分數代表什麼？</h1>

<v-clicks>

<div style="display:flex; flex-direction:column; gap:16px;">
<div style="background:white; border:1px solid #fecaca; border-left:4px solid #dc2626; border-radius:12px; padding:16px 20px; display:flex; align-items:flex-start; gap:16px;">
<span style="background:#dc2626; color:white; padding:4px 14px; border-radius:20px; font-size:0.8rem; font-weight:700; white-space:nowrap; flex-shrink:0;">7-8 分以上</span>
<div>
<p style="font-size:0.95rem; color:#374151; margin:0; line-height:1.6;">工作流非常混亂，<strong style="color:#1a1a1a;">改善空間最大</strong></p>
</div>
</div>

<div style="background:white; border:1px solid #fed7aa; border-left:4px solid #ea580c; border-radius:12px; padding:16px 20px; display:flex; align-items:flex-start; gap:16px;">
<span style="background:#ea580c; color:white; padding:4px 14px; border-radius:20px; font-size:0.8rem; font-weight:700; white-space:nowrap; flex-shrink:0;">4-6 分</span>
<div>
<p style="font-size:0.95rem; color:#374151; margin:0; line-height:1.6;">有基礎但有盲區，有些環節你自己都沒意識到在浪費時間</p>
</div>
</div>

<div style="background:white; border:1px solid #ddd6fe; border-left:4px solid #7c3aed; border-radius:12px; padding:16px 20px; display:flex; align-items:flex-start; gap:16px;">
<span style="background:#7c3aed; color:white; padding:4px 14px; border-radius:20px; font-size:0.8rem; font-weight:700; white-space:nowrap; flex-shrink:0;">0-3 分</span>
<div>
<p style="font-size:0.95rem; color:#374151; margin:0; line-height:1.6;">已經很強，今天幫你更強</p>
</div>
</div>
</div>

</v-clicks>

<div v-click style="margin-top:24px; padding:14px 20px; background:rgba(124,58,237,0.06); border-radius:12px; border:1px solid rgba(124,58,237,0.12);">
<p style="margin:0; font-size:0.9rem; color:#374151; font-style:italic;">「不管幾分，今天我都會告訴你問題在哪、怎麼解決。」</p>
</div>

  </div>
</div>

<!--
等留言分數出現。確認大家都做完了，簡單解讀一下，帶入「工作流」這個主題。
-->

---

<!-- S08 你有哪些？── 白底，checklist 深色卡片 -->
<div class="deco-circles w-full h-full" style="background:#fafafa; padding:60px 80px; position:relative; overflow:hidden;">
  <div style="position:relative; z-index:1;">
<span class="label label-purple" style="margin-bottom:16px; display:inline-block;">開場互動</span>
<h1 style="font-size:2.8rem; font-weight:900; color:#1a1a1a; margin:0 0 32px;">你有哪些？</h1>

<v-clicks>

<div style="display:flex; flex-direction:column; gap:12px;">
<div class="checklist-item">
<div class="checklist-icon" style="background:rgba(124,58,237,0.3);">🎓</div>
<span style="font-size:1rem; font-weight:500;">買過課沒看完</span>
</div>

<div class="checklist-item">
<div class="checklist-icon" style="background:rgba(124,58,237,0.3);">🤖</div>
<span style="font-size:1rem; font-weight:500;">用了 AI 不知道怎麼套工作</span>
</div>

<div class="checklist-item">
<div class="checklist-icon" style="background:rgba(234,88,12,0.3);">💬</div>
<span style="font-size:1rem; font-weight:500;">貼提示詞結果不像人說的話</span>
</div>

<div class="checklist-item">
<div class="checklist-icon" style="background:rgba(234,88,12,0.3);">🌙</div>
<span style="font-size:1rem; font-weight:500;">下班腦袋還在轉</span>
</div>

<div class="checklist-item">
<div class="checklist-icon" style="background:rgba(220,38,38,0.3);">📱</div>
<span style="font-size:1rem; font-weight:500;">LINE + Email 永遠 999+</span>
</div>
</div>

</v-clicks>

<div v-click style="margin-top:24px; text-align:center;">
<span style="font-size:1.2rem; font-weight:900; color:#ea580c;">有的打 1</span>
</div>

  </div>
</div>

<!--
讓大家在留言區打 1，建立「老魚懂我」的共鳴感。等留言湧入再繼續。
-->

---
layout: stage
stage: 2
from: 觀望
to: 開放
subtitle: 三段失敗故事（全部保留不動）
note: 「你憑什麼？」→「你跟我一樣，你也摔過」

---

<!--
這個頁面是隱性的心理轉場：讓觀眾從「我要不要繼續聽」變成「這個人跟我一樣」。
不用多說，直接帶入故事。
-->

---
layout: chapter
chapter: 1
title: 三段人生故事
subtitle: 從 20 幾歲到 48 歲的迴圈

---

<!--
S09。深藍章節頁，標誌性的大字排版。
-->

---
layout: story
label: 第一次低潮
icon: 🏪
---

<!-- S10 第一次低潮：化妝品店 -->
# 退伍，開了一家化妝品店

<v-clicks>

- 退伍金 30 萬 → 開店 → 不到兩年失敗
- 刷信用卡進貨 + 買房 → 欠債 3-400 萬
- 催收電話每天響，存證信函寄到家

</v-clicks>

<!--
S10。語氣平靜地說，不要過度戲劇化。這些事情已經過去了。
-->

---

<!-- S11-S12 第一次低潮：細節 ── 白底，左文右模擬 UI -->
<div class="deco-circles w-full h-full" style="background:#fafafa; padding:60px 80px; position:relative; overflow:hidden;">
  <div style="position:relative; z-index:1; display:grid; grid-template-columns:1fr 1fr; gap:48px; align-items:start; height:100%;">
<!-- 左側文字 -->
<div>
  <p style="color:#7c3aed; font-size:0.85rem; font-weight:700; letter-spacing:0.05em; margin:0 0 12px;">第一次低潮 · 繼續</p>
  <h1 style="font-size:2.4rem; font-weight:900; color:#1a1a1a; margin:0 0 28px; line-height:1.3;">信用破產，<br />每天催收電話響不停</h1>

<v-clicks>

<div style="display:flex; flex-direction:column; gap:12px;">
<p style="font-size:1rem; color:#4b5563; margin:0; line-height:1.8;">債務 3-400 萬，還不出來</p>
<p style="font-size:1rem; color:#4b5563; margin:0; line-height:1.8;">銀行每天打來，就像關不掉的鬧鐘</p>
<p style="font-size:1rem; color:#4b5563; margin:0; line-height:1.8;">存證信函一封封寄到家，告訴媽媽：<br />你兒子欠錢了</p>
</div>

</v-clicks>

</div>

<!-- 右側模擬 UI -->
<div style="display:flex; flex-direction:column; gap:12px; padding-top:60px;">
  <div style="align-self:flex-end;">
    <span class="label label-red">債務 3～400 萬</span>
  </div>

<div v-click class="mock-notification">
<div class="mock-icon" style="background:#fee2e2;">📞</div>
<div>
<div style="font-size:0.85rem; font-weight:700; color:#1a1a1a;">XX 銀行催收部</div>
<div style="font-size:0.75rem; color:#dc2626; margin-top:2px;">來電中…</div>
</div>
<div style="margin-left:auto; background:#dc2626; color:white; padding:4px 12px; border-radius:8px; font-size:0.75rem; font-weight:700;">接聽</div>
</div>

<div v-click class="mock-notification">
<div class="mock-icon" style="background:#fef3c7;">✉️</div>
<div>
<div style="font-size:0.85rem; font-weight:700; color:#1a1a1a;">存證信函</div>
<div style="font-size:0.75rem; color:#6b7280; margin-top:2px;">一封接著一封寄來</div>
</div>
</div>

<div v-click class="mock-notification">
<div class="mock-icon" style="background:#f3f4f6;">😔</div>
<div>
<div style="font-size:0.85rem; font-weight:700; color:#1a1a1a;">告訴媽媽</div>
<div style="font-size:0.75rem; color:#6b7280; margin-top:2px;">你兒子欠錢了</div>
</div>
</div>

</div>
  </div>
</div>

<!--
S11-S12。這一頁用模擬 UI 讓感受更具體——催收電話、存證信函、打電話給媽媽。讓觀眾代入當時的情境。
-->
