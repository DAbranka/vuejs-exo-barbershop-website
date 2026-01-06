<script setup>
import SectionOneCards from "./SectionOneCards.vue";
import SectionTitleSubTitle from "./SectionTitleSubTitle.vue";
</script>

<template>
  <div>
    <section>
      <SectionTitleSubTitle>
        <template #title>Why Choose Us?</template>
        <template #subtitle>
          Excellence in every detail
        </template>
      </SectionTitleSubTitle>
    </section>
    <section>
      <SectionOneCards />
    </section>
  </div>
</template>

<style scoped></style>
