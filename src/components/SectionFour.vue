<script setup>
  import SectionTitleSubTitle from './SectionTitleSubTitle.vue';
  import SectionFourCards from './SectionFourCards.vue';
</script>

<template>
  <div>
    <section>
      <SectionTitleSubTitle>
        <template #title>Client Reviews</template>
        <template #subtitle>What our clients say</template>
      </SectionTitleSubTitle>
    </section>

    <section>
      <SectionFourCards />
    </section>
  </div>
</template>
