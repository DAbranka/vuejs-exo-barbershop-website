<script setup>
import {ref, onMounted, onUnmounted} from "vue";
import CtaBtn from "./CtaBtn.vue";

const activeLink = ref("#hero");
const navBarHeight = 64;
const sections = ['hero', 'section1', 'section2', 'section3', 'section4', 'section5'];

const setActiveLink = (href) => {
  activeLink.value = href;

  // Récupérer l'élément cible
  const targetId = href.replace('#', '');
  const targetElement = document.getElementById(targetId);

  if (targetElement) {
    // Calculer la position avec l'offset
    const elementPosition = targetElement.getBoundingClientRect().top + window.scrollY;
    const offsetPosition = elementPosition - navBarHeight;

    // Scroller vers la position avec offset
    window.scrollTo({
      top: offsetPosition,
      behavior: 'smooth'
    });
  }
};

// Fonction pour détecter quelle section est dans la viewport
const updateActiveSection = () => {
  let currentSection = '#hero';

  for (const sectionId of sections) {
    const element = document.getElementById(sectionId);
    if (element) {
      const rect = element.getBoundingClientRect();
      // Si le top de la section est dans les 200px du haut (offset pour la navbar)
      if (rect.top <= 200 && rect.bottom >= 0) {
        currentSection = `#${sectionId}`;
        break;
      }
    }
  }

  activeLink.value = currentSection;
};

// Ajouter l'écouteur de scroll au montage du composant
onMounted(() => {
  window.addEventListener('scroll', updateActiveSection);
  updateActiveSection(); // Initialiser au montage
});

// Nettoyer l'écouteur au démontage
onUnmounted(() => {
  window.removeEventListener('scroll', updateActiveSection);
});

</script>

/* -------------------------------- TEMPLATE -------------------------------- */
<template>
  <nav class="nav-bar">
    <div class="nav-bar--content">
      <!-- LOGO -->
      <div class="nav-bar-logo--container">
        <!-- <div>
          <img src="" alt="logo/png" />
        </div> -->
        <div class="logo-title">
          <a href="#hero">The Gentlemen's Cut</a>
        </div>
      </div>

      <!-- NAV LINKS -->
      <ul class="nav-list">
        <li class="nav-item">
          <a
            href="#section1"
            :class="{active: activeLink === '#section1'}"
            @click.prevent="setActiveLink('#section1')"
            >About</a
          >
        </li>
        <li class="nav-item">
          <a
            href="#section2"
            :class="{active: activeLink === '#section2'}"
            @click.prevent="setActiveLink('#section2')"
            >Services</a
          >
        </li>
        <li class="nav-item">
          <a
            href="#section4"
            :class="{active: activeLink === '#section4'}"
            @click.prevent="setActiveLink('#section4')"
            >Reviews</a
          >
        </li>
        <li class="nav-item">
          <a
            href="#section5"
            :class="{active: activeLink === '#section5'}"
            @click.prevent="setActiveLink('#section5')"
            >Contact</a
          >
        </li>
      </ul>

      <!-- BOOKING BUTTON -->
      <div class="nav-bar-cta--container">
        <CtaBtn :style="{backgroundColor: 'hsl(from var(--accent) h s l / 1)', fontWeight: 'bold'}"
          >Book Now</CtaBtn
        >
      </div>
    </div>
  </nav>
</template>

/* --------------------------------- STYLE ---------------------------------- */
<style scoped>
.nav-bar {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 20;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: hsl(from var(--black-color) h s 3 / 1);
  color: hsl(from var(--white-color) h s 35 / 1);
  padding: 12px 0;
  border-bottom: 1px solid hsl(from var(--white-color) h s 20 / 1);
}

.nav-bar--content {
  width: 100%;
  max-width: 1200px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav-list {
  list-style: none;
  gap: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.nav-bar-logo--container {
  display: flex;
  align-items: center;
}

.logo-title a{
  margin-left: 10px;
  font-size: 1.5rem;
  font-weight: bold;
  color: hsl(from var(--white-color) h s l / 1);
}

a {
  text-decoration: none;
  color: hsl(from var(--white-color) h s 50 / 1);
  font-weight: 400;
  cursor: pointer;
  transition: color 0.3s ease;
}

a:hover {
  color: var(--accent);
}

a.active {
  color: var(--accent);
}
</style>
