<script setup>
import SectionTwoCard from "./SectionTwoCard.vue";
</script>
<template>
  <div class="cardsSection--wrapper">
    <article>
      <SectionTwoCard>
        <template #title>Signature Cut</template>
        <template #price>40$</template>
        <template #time>45 min</template>
      </SectionTwoCard>
    </article>
    <article>
      <SectionTwoCard>
        <template #title>Beard Design</template>
        <template #price>30$</template>
        <template #time>30 min</template>
      </SectionTwoCard>
    </article>
    <article>
      <SectionTwoCard>
        <template #title>Classic Shave</template>
        <template #price>35$</template>
        <template #time>40 min</template>
      </SectionTwoCard>
    </article>
    <article>
      <SectionTwoCard>
        <template #title>Kids Cut</template>
        <template #price>25$</template>
        <template #time>30 min</template>
      </SectionTwoCard>
    </article>
    <article>
      <SectionTwoCard>
        <template #title>Deluxe Package</template>
        <template #price>75$</template>
        <template #time>90 min</template>
      </SectionTwoCard>
    </article>
    <article>
      <SectionTwoCard>
        <template #title>Hair color</template>
        <template #price>60$</template>
        <template #time>60 min</template>
      </SectionTwoCard>
    </article>
  </div>
</template>

<style scoped>
.cardsSection--wrapper {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: repeat(2, 1fr);
  grid-column-gap: 16px;
  grid-row-gap: 16px;
  padding: 2rem;
}

article {
  background-color: var(--black-color);
  border: 1px solid hsl(from var(--white-color) h s 30 / 1);
  padding: 2rem;
  border-radius: 15px;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 1rem;
}

article:hover {
  border: 1px solid var(--accent);
  cursor: pointer;
  transition: border 0.3s ease;
}
</style>
