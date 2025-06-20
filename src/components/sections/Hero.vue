<template>
  <section class="hero">
    <div class="container">
      <h1 class="hero-title">WenSheng</h1>
      <p class="hero-subtitle">Full Stack Developer</p>
      <div class="hero-location">
        <MapPin class="hero-location-icon" :size="16" />
        <span>Taiwan Kaohsiung</span>
      </div>
      <p class="hero-description">
        我是一名專業的全端工程師，專精於現代網頁應用程式開發。我致力於創造實用、使用者友善的解決方案，幫助企業提升營運效率並達成數位轉型目標。
      </p>
      <div class="hero-buttons">
        <a href="#contact" class="hero-button hero-button-primary">
          <Mail class="hero-button-icon" />
          Hire Me
        </a>
        <a
          href="https://github.com"
          target="_blank"
          class="hero-button hero-button-secondary"
        >
          <github class="hero-button-icon" />
          GitHub
        </a>
        <a
          href="https://linkedin.com"
          target="_blank"
          class="hero-button hero-button-secondary"
        >
          <linkedin class="hero-button-icon" />
          LinkedIn
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
import { MapPin, Mail, github, linkedin } from "lucide-vue-next";
</script>

<style scoped>
.hero {
  padding: var(--space-2xl) 0;
  text-align: left;
}

.hero-title {
  font-size: var(--text-5xl);
  font-weight: 700;

  color: var(--color-text-primary);
}

.hero-subtitle {
  font-size: var(--text-2xl);
  color: var(--color-text-secondary);
  margin-bottom: var(--space-sm);
  font-weight: 400;
}

.hero-location {
  display: flex;
  align-items: center;
  gap: var(--space-xs);
  font-size: var(--text-lg);
  color: var(--color-text-secondary);
  margin-bottom: var(--space-sm);
}

.hero-location-icon {
  width: 20px;
  height: 20px;
  opacity: 0.7;
}

.hero-description {
  font-size: var(--text-lg);
  color: var(--color-text-secondary);
  margin-bottom: var(--space-sm);
  line-height: 1.6;
}

.hero-buttons {
  display: flex;
  gap: var(--space-sm);
  flex-wrap: wrap;
}

.hero-button {
  display: flex;
  align-items: center;
  gap: var(--space-xs);
  padding: var(--space-xs) var(--space-sm);
  border-radius: 0.5rem;
  text-decoration: none;
  font-weight: 500;
  font-size: var(--text-base);
  transition: all var(--transition-fast);
  border: 1px solid var(--color-border);
}

.hero-button-primary {
  background-color: var(--color-text-primary);
  color: var(--color-primary);
}

.hero-button-primary:hover {
  background-color: var(--color-text-secondary);
}

.hero-button-secondary {
  background-color: transparent;
  color: var(--color-text-secondary);
}

.hero-button-secondary:hover {
  background-color: var(--color-secondary);
  color: var(--color-text-primary);
}

.hero-button-icon {
  width: 18px;
  height: 18px;
}
</style>
