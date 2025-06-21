<template>
  <section id="projects" class="section">
    <div class="container">
      <h2 class="section-title">精選作品</h2>
      <div class="projects-grid">
        <div class="project-card">
          <div class="project-image">
            <span>專案截圖</span>
          </div>
          <div class="project-content">
            <h3 class="project-title">電商平台</h3>
            <p class="project-description">
              使用 React 和 Node.js 開發的全功能電商平台，
              包含購物車、付款系統和後台管理功能。
            </p>
            <div class="project-tech">
              <span class="tech-tag">React</span>
              <span class="tech-tag">Node.js</span>
              <span class="tech-tag">MongoDB</span>
              <span class="tech-tag">Stripe</span>
            </div>
          </div>
        </div>
        <div class="project-card">
          <div class="project-image">
            <span>專案截圖</span>
          </div>
          <div class="project-content">
            <h3 class="project-title">任務管理系統</h3>
            <p class="project-description">
              團隊協作工具，具備任務分配、進度追蹤、
              即時通訊等功能的專案管理平台。
            </p>
            <div class="project-tech">
              <span class="tech-tag">Vue.js</span>
              <span class="tech-tag">Firebase</span>
              <span class="tech-tag">Socket.io</span>
              <span class="tech-tag">Tailwind</span>
            </div>
          </div>
        </div>
        <div class="project-card">
          <div class="project-image">
            <span>專案截圖</span>
          </div>
          <div class="project-content">
            <h3 class="project-title">數據視覺化儀表板</h3>
            <p class="project-description">
              互動式數據儀表板，支援多種圖表類型，
              即時數據更新和自定義配置功能。
            </p>
            <div class="project-tech">
              <span class="tech-tag">D3.js</span>
              <span class="tech-tag">React</span>
              <span class="tech-tag">Python</span>
              <span class="tech-tag">PostgreSQL</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style>
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: var(--space-lg);
}

.project-card {
  background-color: var(--color-secondary);
  border-radius: 0.5rem;
  overflow: hidden;
  border: 1px solid var(--color-border);
  transition: transform var(--transition-fast);
}

.project-card:hover {
  border-color: var(--color-text-secondary);
}

.project-image {
  width: 100%;
  height: 200px;
  background-color: var(--color-hover);
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--color-text-secondary);
}

.project-content {
  padding: var(--space-lg);
}

.project-title {
  font-size: var(--text-xl);
  font-weight: 600;
  margin-bottom: var(--space-xs);
}

.project-description {
  color: var(--color-text-secondary);
  margin-bottom: var(--space-sm);
}

.project-tech {
  display: flex;
  flex-wrap: wrap;
  gap: var(--space-xs);
}

.tech-tag {
  background-color: var(--color-hover);
  color: var(--color-text-secondary);
  padding: 0.25rem 0.5rem;
  border-radius: 0.25rem;
  font-size: var(--text-xs);
}
</style>
