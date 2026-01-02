<script setup lang="ts">
import HeaderTitle from "./HeaderTitle.vue";
import CtaBtn from "./CtaBtn.vue";
</script>

<template>
  <!-- TITLE -->
  <div class="hdrTitle">
    <HeaderTitle>Where Style Meets Tradition</HeaderTitle>
    <section class="ctaSection">
      <ul>
        <li>
          <CtaBtn :style="{backgroundColor: 'var(--accent)'}">Get Started</CtaBtn>
        </li>
        <li>
          <CtaBtn>Learn More</CtaBtn>
        </li>
      </ul>
    </section>
  </div>

  <!-- IMG / VIDEO -->
  <div class="bgMedia">
    <!-- Background media goes here -->
    <div>
      <img
        src="https://res.cloudinary.com/planity/image/upload/c_crop,w_2048,h_1219,x_0,y_0/q_auto,f_auto/jupjkgzwa8vmqlunuxon"
        alt="Barber Shop Background"
      />
    </div>
  </div>
</template>

<style scoped>
.hdrTitle {
  position: absolute;
  top: 0;
  left: 0;
  color: var(--white-color);
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
  font-size: 3rem;
  z-index: 1;
  overflow: hidden;
}

.ctaSection ul {
  list-style: none;
  display: flex;
  gap: 20px;
  margin-top: 20px;
  padding: 0;
}

.bgMedia {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
  z-index: -1;
  display: flex;
  justify-content: center;
  align-items: center;
}

.bgMedia img {
  height: 100%;
  object-fit: cover;
  filter: brightness(0.7);
}
</style>
