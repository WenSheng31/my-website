<template>
  <section id="experience" class="section">
    <div class="container">
      <h2 class="section-title">工作經歷</h2>
      <div class="experience-timeline">
        <div class="experience-item">
          <div class="experience-period">2022 - 至今</div>
          <h3 class="experience-title">資深前端工程師</h3>
          <div class="experience-company">科技創新公司</div>
          <p class="experience-description">
            負責公司主要產品的前端開發工作，包括架構設計、效能優化、
            團隊技術指導等。成功提升產品載入速度 40%，使用者滿意度顯著提升。
          </p>
        </div>
        <div class="experience-item">
          <div class="experience-period">2020 - 2022</div>
          <h3 class="experience-title">前端工程師</h3>
          <div class="experience-company">數位媒體公司</div>
          <p class="experience-description">
            參與多個大型網站專案的開發，熟悉敏捷開發流程，
            與設計師和後端工程師密切協作，確保專案順利交付。
          </p>
        </div>
        <div class="experience-item">
          <div class="experience-period">2018 - 2020</div>
          <h3 class="experience-title">初級前端工程師</h3>
          <div class="experience-company">新創公司</div>
          <p class="experience-description">
            從零開始學習前端開發，快速掌握各種技術框架，
            積極參與程式碼審查和技術分享，奠定了紮實的技術基礎。
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
.experience-timeline {
  max-width: 800px;
  margin: 0;
}

.experience-item {
  border-left: 2px solid var(--color-border);
  padding-left: var(--space-lg);
  margin-bottom: var(--space-xl);
  position: relative;
}

.experience-item::before {
  content: "";
  position: absolute;
  left: -6px;
  top: 0;
  width: 10px;
  height: 10px;
  background-color: var(--color-text-primary);
  border-radius: 50%;
}

.experience-period {
  color: var(--color-text-secondary);
  font-size: var(--text-sm);
  margin-bottom: var(--space-xs);
}

.experience-title {
  font-size: var(--text-xl);
  font-weight: 600;
  margin-bottom: var(--space-xs);
}

.experience-company {
  color: var(--color-text-secondary);
  margin-bottom: var(--space-sm);
}

.experience-description {
  color: var(--color-text-secondary);
}
</style>
