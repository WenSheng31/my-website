<template>
  <section id="skills" class="section">
    <div class="container">
      <h2 class="section-title">專業技能</h2>
      <div class="skills-grid">
        <div class="skill-card">
          <h3 class="skill-title">前端開發</h3>
          <p class="skill-description">
            熟練掌握 HTML5、CSS3、JavaScript (ES6+)、TypeScript， 以及
            React、Vue.js 等現代前端框架。
          </p>
        </div>
        <div class="skill-card">
          <h3 class="skill-title">UI/UX 設計</h3>
          <p class="skill-description">
            具備良好的設計美感，熟悉 Figma、Adobe XD 等設計工具，
            能夠設計出美觀且易用的介面。
          </p>
        </div>
        <div class="skill-card">
          <h3 class="skill-title">響應式設計</h3>
          <p class="skill-description">
            精通 CSS Grid、Flexbox 和 Tailwind CSS，
            能夠創建適應各種螢幕尺寸的響應式網頁。
          </p>
        </div>
        <div class="skill-card">
          <h3 class="skill-title">效能優化</h3>
          <p class="skill-description">
            深入了解網頁效能優化技巧，包括程式碼分割、懶載入、
            圖片優化等最佳實踐。
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: var(--space-lg);
}

.skill-card {
  background-color: var(--color-secondary);
  padding: var(--space-lg);
  border-radius: 0.5rem;
  border: 1px solid var(--color-border);
  transition: transform var(--transition-fast);
}

.skill-card:hover {
  border-color: var(--color-text-secondary);
}

.skill-title {
  font-size: var(--text-xl);
  font-weight: 600;
  margin-bottom: var(--space-sm);
}

.skill-description {
  color: var(--color-text-secondary);
}
</style>
