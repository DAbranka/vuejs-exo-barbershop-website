<template>
  <div>
    <section>
      <div data-icon><slot name="icon">Icon</slot></div>
    </section>
    <section>
      <p data-title><slot name="title">Title</slot></p>
    </section>
    <section>
      <p data-description><slot name="description">Description</slot></p>
    </section>
  </div>
</template>

<style scoped>
div:not([data-icon]) {
  background-color: hsl(from var(--black-color) h s 7 / 1);
  padding: 2rem;
  border-radius: 15px;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 1rem;
  border: 1px solid hsl(from var(--white-color) h s 20 / 1);
}

p[data-title] {
  font-size: 1.3rem;
  font-weight: bold;
}

p[data-description] {
  font-size: 1rem;
  line-height: 1.5;
  color: hsl(from var(--white-color) h s 75 / 1);
}
</style>
