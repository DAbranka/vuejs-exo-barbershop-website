<script setup></script>

<template>
  <div>
    <section>
      <span>★★★★★</span>
    </section>
    <section>
      <q><slot name="quote">Quote</slot></q>
    </section>
    <section>
      <p><slot name="author">Author</slot></p>
    </section>
  </div>
</template>

<style scoped>
q {
  font-style: italic;
  font-size: 1rem;
  line-height: 1.5;
  color: hsl(from var(--white) h s 80/ 1);
  display: block;
  margin-top: 1rem;
}

span {
  color: #f58a18;
  font-size: 1.5rem;
}

p {
  margin-top: 1rem;
  font-weight: 400;
  color: var(--white-color);
}
</style>
