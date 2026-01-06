<script setup>
import SectionTitleSubTitle from "./SectionTitleSubTitle.vue";
import SectionTwoCards from "./SectionTwoCards.vue";
</script>

<template>
  <div>
    <section>
      <SectionTitleSubTitle>
        <template #title>Our Services</template>
        <template #subtitle> Tailored grooming for every gentleman </template>
      </SectionTitleSubTitle>
    </section>

    <section>
      <SectionTwoCards />
    </section>
  </div>
</template>

<style scoped></style>
