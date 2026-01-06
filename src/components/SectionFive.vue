<script setup>
import SectionTitleSubTitle from "./SectionTitleSubTitle.vue";
import CtaBtn from "./CtaBtn.vue";
</script>
<template>
  <div>
    <section>
      <SectionTitleSubTitle>
        <template #title>Ready for a Fresh Look</template>
        <template #subtitle
          >Visit us at 456 Oak Avenue, Downtown - Open 7 days a week - Call us at (123)
          456-7890</template
        >
      </SectionTitleSubTitle>
    </section>

    <section>
      <div class="section-five-cta--container">
        <CtaBtn
          :style="{
            backgroundColor: 'hsl(from var(--accent) h s l / 1)',
            fontWeight: 'bold',
            fontSize: '1.2rem',
            padding: '1rem 2rem',
          }"
          >Book Your Appointment Today</CtaBtn
        >
      </div>
    </section>

    <section class="socialMedia">
      <!-- Social media links could go here -->
      
    </section>
  </div>
</template>
<style scoped>
.section-five-cta--container {
  display: flex;
  justify-content: center;
  padding: 2rem;
}
</style>
