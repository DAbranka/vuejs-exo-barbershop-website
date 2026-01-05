<script setup lang="ts">
import SectionOneCard from "./SectionOneCard.vue";
import SectionTitleSubTitle from "./SectionTitle&SubTitle.vue";
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
      <article>
        <SectionOneCard />
      </article>
    </section>
  </div>
</template>

<style scoped></style>
