<template>
  <section id="about" class="section">
    <div class="container">
      <h2 class="section-title">關於我</h2>
      <div class="about-content">
        <div class="about-text">
          <p>
            我是一名充滿熱忱的前端工程師，擁有豐富的網頁開發經驗。專精於現代前端技術，包括
            React、Vue.js、以及各種 CSS 框架。
          </p>
          <br />
          <p>
            我相信優秀的設計不僅要視覺上令人印象深刻，更要在功能性和使用者體驗上達到完美平衡。每一個專案都是我對完美追求的體現。
          </p>
          <br />
          <p>
            除了技術能力，我也重視團隊協作和持續學習，時刻關注業界最新趨勢，確保我的技能始終保持在最前沿。
          </p>
        </div>
        <div class="about-image">
          <span>個人照片</span>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: var(--space-xl);
  align-items: center;
}

.about-text {
  font-size: var(--text-lg);
  color: var(--color-text-secondary);
  line-height: 1.8;
}

.about-image {
  width: 100%;
  height: 400px;
  background-color: var(--color-secondary);
  border-radius: 0.5rem;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--color-text-secondary);
}
</style>
