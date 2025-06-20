<template>
  <header class="header">
    <nav class="nav container">
      <div class="nav-left">
        <h1 class="logo">WENSHENG</h1>
        <ul class="nav-links">
          <li><a href="#about" class="nav-link">About</a></li>
          <li><a href="#skills" class="nav-link">Skills</a></li>
          <li><a href="#projects" class="nav-link">Projects</a></li>
          <li><a href="#experience" class="nav-link">Experience</a></li>
        </ul>
      </div>
      <button class="cta-button">Contact Me</button>
    </nav>
  </header>
</template>

<style scoped>
.header {
  position: sticky;
  top: 0;
  width: 100%;
  background-color: var(--color-primary);
  border-bottom: 1px solid var(--color-border);
  z-index: 1000;
  backdrop-filter: blur(10px);
}

.nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: var(--header-height);
  padding: 0 var(--space-sm);
}

.nav-left {
  display: flex;
  align-items: center;
  gap: var(--space-lg);
}

.logo {
  font-size: var(--text-base);
  font-weight: 600;
  color: var(--color-text-primary);
  letter-spacing: 0.05em;
}

.nav-links {
  display: flex;
  list-style: none;
  gap: var(--space-md);
}

.nav-link {
  text-decoration: none;
  color: var(--color-text-secondary);
  font-weight: 500;
  font-size: var(--text-sm);
  transition: color var(--transition-fast);
}

.nav-link:hover {
  color: var(--color-text-primary);
}

.cta-button {
  background-color: var(--color-primary);
  color: var(--color-text-primary);
  padding: var(--space-xs) var(--space-sm);
  border: 1px solid var(--color-border);
  border-radius: 0.375rem;
  font-weight: 500;
  font-size: var(--text-sm);
  cursor: pointer;
  transition: all var(--transition-fast);
}

.cta-button:hover {
  background-color: var(--color-hover);
  border-color: var(--color-text-secondary);
}
</style>
