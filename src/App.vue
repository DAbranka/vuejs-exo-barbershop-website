<script setup>
import TitleBg from "./components/TitleBg.vue";
import SectionComp from "./components/SectionComp.vue";
import FooterComp from "./components/FooterComp.vue";
import NavBar from "./components/NavBar.vue";
</script>

<template>
  <!-- HEADER -->
  <header id="hero">
    <NavBar />
    <TitleBg />
  </header>

  <!-- MAIN CONTENT -->
  <main>
    <SectionComp id="section1">SECTION 1</SectionComp>
    <SectionComp id="section2">SECTION 2</SectionComp>
    <SectionComp id="section3">SECTION 3</SectionComp>
  </main>

  <!-- FOOTER -->
  <footer>
    <FooterComp />
  </footer>
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html,
body,
#app {
  height: 100%;
  font-family: var(--font-primary);
  scroll-behavior: smooth;
}

:root {
  --primary-color: #010101;
  --secondary-color: #f5f5f5;
  --accent: hsl(8, 100%, 52%);
  --black-color: #000000;
  --white-color: #ffffff;
  --font-primary: 'Helvetica Neue', Helvetica, Arial, sans-serif;
  --font-secondary: 'Georgia', serif;
}

header {
  position: relative;
  height: 100%;
}

#section1 {
  background-color: #ffdddd;
  height: 100vh;
}
#section2 {
  background-color: #ddffdd;
  height: 100vh;
}
#section3 {
  background-color: #ddddff;
  height: 100vh;
}
#section4 {
  background-color: #ffffdd;
  height: 100vh;
}
</style>
