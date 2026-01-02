<script setup>
import {ref} from "vue";

const activeLink = ref("#hero");

const setActiveLink = (href) => {
  activeLink.value = href;
};
</script>

/* -------------------------------- TEMPLATE -------------------------------- */
<template>
  <nav class="nav-bar">
    <ul class="nav-list">
      <li class="nav-item">
        <a
          href="#hero"
          :class="{active: activeLink === '#hero'}"
          @click="setActiveLink('#hero')"
          >Acceuil</a
        >
      </li>
      <li class="nav-item">
        <a
          href="#section1"
          :class="{active: activeLink === '#section1'}"
          @click="setActiveLink('#section1')"
          >About</a
        >
      </li>
      <li class="nav-item">
        <a
          href="#section2"
          :class="{active: activeLink === '#section2'}"
          @click="setActiveLink('#section2')"
          >Services</a
        >
      </li>
      <li class="nav-item">
        <a
          href="#section3"
          :class="{active: activeLink === '#section3'}"
          @click="setActiveLink('#section3')"
          >Contact</a
        >
      </li>
    </ul>
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
  align-content: center;
  padding: 20px 20px;
}

.nav-list {
  list-style: none;
  gap: 20px;
  margin: 0;
  padding: 0;
  display: flex;
  background-color: var(--black-color);
  padding: 20px 40px;
  border-radius: 40px;
}

a {
  text-decoration: none;
  color: var(--white-color);
  font-weight: bold;
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
