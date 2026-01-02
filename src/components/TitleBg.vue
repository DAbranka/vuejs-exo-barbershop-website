<script setup lang="ts">
import HeaderTitle from "./HeaderTitle.vue";
import CtaBtn from "./CtaBtn.vue";
</script>

<template>
  <!-- TITLE -->
  <div class="hdrTitle">
    <HeaderTitle>HEADER TITLE</HeaderTitle>
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
    <video autoplay loop muted>
      <!-- Put your video source here -->
      <source src="/src/assets/video/bg-video.mp4" type="video/mp4" />
      Your browser does not support the video tag.
    </video>
  </div>
</template>

<style scoped>
.hdrTitle {
  position: absolute;
  top: 0;
  left: 0;
  color: var(--black-color);
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100%;
  font-size: 3rem;
  z-index: 1;
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
}

.bgMedia video {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
