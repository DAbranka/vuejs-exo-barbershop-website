<script setup lang="ts">
import SectionFourImgGal from "./SectionFourImgGal.vue";
import SectionTitleSubTitle from "./SectionTitleSubTitle.vue";
</script>

<template>
  <div>
    <section>
      <SectionTitleSubTitle>
        <template #title>Our Athmosphere</template>
        <template #subtitle> Step into excellence </template>
      </SectionTitleSubTitle>
    </section>
    <section>
      <SectionFourImgGal />
    </section>
  </div>
</template>

<style scoped></style>
