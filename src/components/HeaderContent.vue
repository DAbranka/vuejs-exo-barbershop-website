<script setup lang="ts">
import HeaderTitle from "./HeaderTitle.vue";
import CtaBtn from "./CtaBtn.vue";
</script>

<template>
  <section class="headerContent">
    <!-- Textual Content -->
    <section class="hdrTitle">
      <HeaderTitle>Where Style <br> Meets Tradition</HeaderTitle>
      <article>
        <p>
          Experience the art of grooming at our barber shop, where skilled
          barbers blend classic techniques with modern styles to give you a look
          that’s uniquely you.
        </p>
      </article>
      <section class="ctaSection">
        <ul>
          <li>
            <CtaBtn :style="{backgroundColor: 'hsl(from var(--accent) h s l / 1)'}"
              >Shedule Appointment</CtaBtn
            >
          </li>
          <li>
            <CtaBtn>View Pricing</CtaBtn>
          </li>
        </ul>
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
  margin-top: 20px;
  font-size: 1.4rem;
  line-height: 1.6;
  font-family: var(--font-secondary);
  color: hsl(from var(--white-color) h s 50 / 1);

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
