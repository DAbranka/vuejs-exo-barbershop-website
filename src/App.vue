<script setup>
import FooterComp from "./components/FooterComp.vue";
import NavBar from "./components/NavBar.vue";
import HeaderContent from "./components/HeaderContent.vue";
import SectionOne from "./components/SectionOne.vue";
import SectionTwo from "./components/SectionTwo.vue";
import SectionThree from "./components/SectionThree.vue";
import SectionFour from "./components/SectionFour.vue";
</script>

<template>
  <!-- HEADER -->
  <header id="hero">
    <NavBar />
    <HeaderContent />
  </header>

  <!-- MAIN CONTENT -->
  <main>
    <SectionOne id="section1" />
    <SectionTwo id="section2" />
    <SectionThree id="section3" />
    <SectionFour id="section4" />
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
  color: var(--white-color);
}

body {
  display: flex;
  justify-content: center;
  background-color: var(--black-color);
}

#app {
  width: 100%;
  max-width: 1200px;
}

:root {
  /* -------------------------------------------------------------------------- */

  --black: #000000;
  --white: #ffffff;
  --black-color: hsl(from var(--black) h s 3 / 1);
  --white-color: #ffffff;

  /* -------------------------------------------------------------------------- */

  --primary-color: #010101;
  --secondary-color: #f5f5f5;
  --accent: hsl(8 75 52);

  /* -------------------------------------------------------------------------- */

  --font-primary: "Helvetica Neue", Helvetica, Arial, sans-serif;
  --font-secondary: "Georgia", serif;

  /* -------------------------------------------------------------------------- */
}

header {
  position: relative;
  height: 100%;
}

#section1,
#section2,
#section3,
#section4 {
  padding-bottom: 2rem;
}

#section1 {
  background-color: #1c1c1c;
}
#section2 {
  background-color: var(--black-color);
}
#section3 {
  background-color: #252525;
}
#section4 {
  background-color: var(--black-color);
}
</style>
