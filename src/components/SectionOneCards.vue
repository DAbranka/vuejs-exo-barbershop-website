<script setup>
import SectionOneCard from "./SectionOneCard.vue";
</script>
<template>
  <ul>
    <li>
      <article>
        <SectionOneCard>
          <template></template>
          <template #title>Award Winning</template>
          <template #description>Recognized for excellence in modern barbering</template>
        </SectionOneCard>
      </article>
    </li>
    <li>
      <article>
        <SectionOneCard>
          <template></template>
          <template #title>Expert Barbers</template>
          <template #description
            >Certified professionals with years of experience</template
          >
        </SectionOneCard>
      </article>
    </li>
    <li>
      <article>
        <SectionOneCard>
          <template></template>
          <template #title>Quick Service</template>
          <template #description
            >Premium service without the wait</template
          >
        </SectionOneCard>
      </article>
    </li>
    <li>
      <article>
        <SectionOneCard>
          <template></template>
          <template #title>Classic Techniques</template>
          <template #description
            >Traditional methods meet modern style</template
          >
        </SectionOneCard>
      </article>
    </li>
  </ul>
</template>

<style scoped>
ul {
  list-style: none;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  padding: 2rem;
}
</style>
