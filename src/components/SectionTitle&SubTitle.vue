<template>
  <section>
    <article>
      <h2><slot name="title">Section Title</slot></h2>
      <h3><slot name="subtitle">Section SubTitle</slot></h3>
    </article>
  </section>
</template>

<style scoped>

  section {
    text-align: center;
    padding: 3rem 0 1.25rem 0;
  }

  h2{
    font-size: 3rem;
    margin-bottom: 0.5rem;
  }

  h3{
    font-size: 1.2rem;
    font-weight: normal;
    color: hsl(from var(--black-color) h s 55 / 1);
  }
</style>
