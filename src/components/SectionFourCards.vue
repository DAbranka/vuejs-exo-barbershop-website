<script setup>
import SectionFourCard from "./SectionFourCard.vue";
</script>

<template>
  <div>
    <ul>
      <li>
        <article>
          <SectionFourCard>
            <template #quote
              >Best barbershop in the city! The attention to detail is
              incredible.</template
            >
            <template #author>Michael Chen</template>
          </SectionFourCard>
        </article>
      </li>
      <li>
        <article>
          <SectionFourCard>
            <template #quote
              >Professional service every time. My go-to place for grooming.</template
            >
            <template #author>James Rodriguez</template>
          </SectionFourCard>
        </article>
      </li>
      <li>
        <article>
          <SectionFourCard>
            <template #quote
              >The barbers here are true artists. Always leave looking sharp!</template
            >
            <template #author>David Kim</template>
          </SectionFourCard>
        </article>
      </li>
    </ul>
  </div>
</template>

<style scoped>
ul {
  list-style: none;
  display: flex;
  gap: 2rem;
  padding: 2rem;
}

article {
  background-color: #1c1c1c;
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
</style>
