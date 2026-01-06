<script setup></script>
<template>
  <section>
    <div id="title">
      <p><slot name="title">Title</slot></p>
    </div>
    <div id="price">
      <p><slot name="price">Price</slot></p>
    </div>
  </section>
  <section>
    <div>
      <p><slot name="time">Time</slot></p>
    </div>
  </section>
</template>

<style scoped>
#title {
  font-weight: 600;
  font-size: 1.5rem;
}

#price {
  font-weight: 500;
  font-size: 1.5rem;
  color: hsl(from var(--accent) h 100 60 / 1);
}

section:first-child {
  display: flex;
  justify-content: space-between;
}
</style>
