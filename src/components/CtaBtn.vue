<template>
  <button class="cta-btn"><slot>Call to Action</slot></button>
</template>

<style scoped>
.cta-btn {
  background-color: var(--black-color);
  color: var(--white-color);
  border: none;
  padding: 12px 24px;
  font-size: 1rem;
  border-radius: 40px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.cta-btn:hover {
  background-color: var(--accent);
}
</style>
