<template>
  <header class="header">
    <nav class="nav container">
      <div class="nav-left">
        <h1 class="logo">WENSHENG</h1>
        <ul class="nav-links" :class="{ 'nav-links-active': isMenuOpen }">
          <li>
            <a href="#about" class="nav-link" @click="closeMenu">About</a>
          </li>
          <li>
            <a href="#skills" class="nav-link" @click="closeMenu">Skills</a>
          </li>
          <li>
            <a href="#projects" class="nav-link" @click="closeMenu">Projects</a>
          </li>
          <li>
            <a href="#experience" class="nav-link" @click="closeMenu"
              >Experience</a
            >
          </li>
        </ul>
      </div>

      <div class="nav-right">
        <button class="cta-button desktop-cta">Contact Me</button>

        <!-- 漢堡選單按鈕 -->
        <button
          class="menu-toggle"
          @click="toggleMenu"
          :class="{ 'menu-toggle-active': isMenuOpen }"
          aria-label="Toggle menu"
        >
          <span class="hamburger-line"></span>
          <span class="hamburger-line"></span>
          <span class="hamburger-line"></span>
        </button>
      </div>
    </nav>

    <!-- 移動端背景遮罩 -->
    <div
      class="menu-overlay"
      :class="{ 'menu-overlay-active': isMenuOpen }"
      @click="closeMenu"
    ></div>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};

const closeMenu = () => {
  isMenuOpen.value = false;
};

// 監聽 ESC 鍵關閉選單
const handleEscKey = (event) => {
  if (event.key === "Escape") {
    closeMenu();
  }
};

// 監聽視窗大小變化，在桌面版時自動關閉選單
const handleResize = () => {
  if (window.innerWidth >= 768) {
    closeMenu();
  }
};

onMounted(() => {
  document.addEventListener("keydown", handleEscKey);
  window.addEventListener("resize", handleResize);
});

onUnmounted(() => {
  document.removeEventListener("keydown", handleEscKey);
  window.removeEventListener("resize", handleResize);
});
</script>

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
  position: relative;
}

.nav-left {
  display: flex;
  align-items: center;
  gap: var(--space-lg);
}

.nav-right {
  display: flex;
  align-items: center;
  gap: var(--space-md);
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
  margin: 0;
  padding: 0;
  transition: all 0.3s ease;
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
  background-color: var(--color-border);
}

/* 漢堡選單按鈕 */
.menu-toggle {
  display: none;
  flex-direction: column;
  justify-content: space-between;
  width: 24px;
  height: 18px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 0;
  z-index: 1001;
}

.hamburger-line {
  width: 100%;
  height: 2px;
  background-color: var(--color-text-primary);
  transition: all 0.3s ease;
  transform-origin: center;
}

.menu-toggle-active .hamburger-line:nth-child(1) {
  transform: rotate(45deg) translate(6px, 6px);
}

.menu-toggle-active .hamburger-line:nth-child(2) {
  opacity: 0;
}

.menu-toggle-active .hamburger-line:nth-child(3) {
  transform: rotate(-45deg) translate(6px, -6px);
}

/* 背景遮罩 */
.menu-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.5);
  opacity: 0;
  visibility: hidden;
  transition: all 0.3s ease;
  z-index: 999;
}

.menu-overlay-active {
  opacity: 1;
  visibility: visible;
}

/* 移動端樣式 */
@media (max-width: 767px) {
  .nav-left {
    gap: 0;
  }

  .nav-links {
    position: fixed;
    top: 0;
    right: -100%;
    width: 280px;
    height: 100vh;
    background-color: var(--color-primary);
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;
    padding: 80px 2rem 2rem;
    box-shadow: -2px 0 10px rgba(0, 0, 0, 0.1);
    transition: right 0.3s ease;
    z-index: 1000;
  }

  .nav-links-active {
    right: 0;
  }

  .nav-link {
    font-size: 1.1rem;
    padding: 0.75rem 0;
    width: 100%;
    border-bottom: 1px solid var(--color-border);
  }

  .nav-link:last-child {
    border-bottom: none;
  }

  .menu-toggle {
    display: flex;
  }

  .desktop-cta {
    display: none;
  }

  /* 在移動端選單中添加 Contact 按鈕 */
  .nav-links::after {
    content: "";
    display: block;
    width: 100%;
    margin-top: 2rem;
  }

  .nav-links-active::after {
    content: "Contact Me";
    background-color: var(--color-primary);
    color: var(--color-text-primary);
    padding: 0.75rem 1rem;
    border: 1px solid var(--color-border);
    border-radius: 0.375rem;
    text-align: center;
    cursor: pointer;
    transition: all var(--transition-fast);
    font-weight: 500;
    font-size: var(--text-sm);
  }
}

/* 平板端適配 */
@media (max-width: 1024px) and (min-width: 768px) {
  .nav {
    padding: 0 var(--space-md);
  }

  .nav-left {
    gap: var(--space-md);
  }

  .nav-links {
    gap: var(--space-sm);
  }
}

/* 防止滾動 */
body.menu-open {
  overflow: hidden;
}
</style>
