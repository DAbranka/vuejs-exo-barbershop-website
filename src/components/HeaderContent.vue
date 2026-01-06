<script setup lang="ts">
import HeaderTitle from "./HeaderTitle.vue";
import CtaBtn from "./CtaBtn.vue";
import {ref} from "vue";

const activeLink = ref("#hero");

const setActiveLink = (href) => {
  activeLink.value = href;

  // Récupérer l'élément cible
  const targetId = href.replace("#", "");
  const targetElement = document.getElementById(targetId);

  if (targetElement) {
    // Hauteur de la navbar (en pixels)
    const navBarHeight = 64; // Ajustez selon votre hauteur réelle

    // Calculer la position avec l'offset
    const elementPosition = targetElement.getBoundingClientRect().top + window.scrollY;
    const offsetPosition = elementPosition - navBarHeight;

    // Scroller vers la position avec offset
    window.scrollTo({
      top: offsetPosition,
      behavior: "smooth",
    });
  }
};
</script>

<template>
  <section class="headerContent">
    <!-- Textual Content -->
    <section class="hdrTitle">
      <!-- Sub Title -->
      <div class="hdrSubTitle">
        <p>✨ Premium Grooming Since 2015</p>
      </div>

      <!-- Header Title -->
      <HeaderTitle
        >Where Style <br />
        Meets Tradition</HeaderTitle
      >

      <!-- Sub Paragraph -->
      <article>
        <p>
          Experience the art of grooming at our barber shop, where skilled barbers blend
          classic techniques with modern styles to give you a look that’s uniquely you.
        </p>
      </article>

      <!-- CTA BUTTONS -->
      <section class="ctaSection">
        <ul>
          <li>
            <CtaBtn :style="{backgroundColor: 'hsl(from var(--accent) h s l / 1)'}"
              >Shedule Appointment</CtaBtn
            >
          </li>
          <li>
            <CtaBtn>
              <a
                :style="{textDecoration: 'none', color: 'inherit'}"
                href="#section2"
                @click.prevent="setActiveLink('#section2')"
                >View Pricing</a
              >
            </CtaBtn>
          </li>
        </ul>
      </section>

      <!-- Stats -->
      <section>
        <article>
          <p>10K+</p>
          <p>Happy Clients</p>
        </article>
        <article>
          <p>15+</p>
          <p>Expert Barbers</p>
        </article>
        <article>
          <p>4.9</p>
          <p>Average Rating</p>
        </article>
      </section>
    </section>

    <!-- IMG / VIDEO -->
    <section class="headerImg--wrapper">
      <!-- Background media goes here -->
      <div class="headerImg__img--wrapper">
        <img
          src="https://res.cloudinary.com/planity/image/upload/c_crop,w_2048,h_1219,x_0,y_0/q_auto,f_auto/jupjkgzwa8vmqlunuxon"
          alt="Barber Shop Background"
        />
      </div>
    </section>
  </section>
</template>

<style scoped>
.headerContent {
  display: flex;
  width: 100%;
  height: 100vh;
  position: relative;
}

.hdrSubTitle p {
  font-size: 1rem;
  color: hsl(from var(--white-color) 40 100 50 / 1);
  margin: 0 0 30px 0;
  font-weight: 500;
  background: #ea650026;
  display: inline-block;
  padding: 10px 15px;
  border-radius: 20px;
}

.hdrTitle {
  color: var(--white-color);
  width: 50%;
  height: 100%;
  z-index: 1;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 0 40px 0 0;
}

.hdrTitle article {
  margin: 20px 0;
  font-size: 1.3rem;
  line-height: 1.55;
  font-family: var(--font-primary);
  color: hsl(from var(--white-color) h s 50 / 1);
}

.hdrTitle section:last-child {
  display: flex;
  margin-top: 30px;
}

.hdrTitle section:last-child article {
  margin-right: 40px;
}
.hdrTitle section:last-child article p:first-child {
  font-size: 2rem;
  font-weight: 700;
  color: hsl(from var(--white-color) h s 90 / 1);
}

.hdrTitle section:last-child article p:last-child {
  font-size: 1rem;
  font-weight: 500;
  color: hsl(from var(--white-color) h s 70 / 1);
}

.ctaSection ul {
  list-style: none;
  display: flex;
  gap: 20px;
  margin-top: 20px;
  padding: 0;
}

.ctaSection ul li > button {
  font-size: 1rem;
  font-weight: 600;
  padding: 20px 40px;
}

.headerImg--wrapper {
  width: 50%;
  height: 100%;
  overflow: hidden;
  z-index: -1;
  display: flex;
  justify-content: center;
  align-items: center;
}

.headerImg__img--wrapper {
  width: 600px;
  height: 600px;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  border-radius: 20px;
}
.headerImg--wrapper img {
  height: 100%;
  width: 100%;
  object-fit: cover;
  filter: brightness(0.7);
}
</style>
