<template>
  <div>
    <div class="imgContainer">
      <img
        src="https://images.unsplash.com/photo-1759134198561-e2041049419c?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w3Nzg4Nzd8MHwxfHNlYXJjaHwxfHxtb2Rlcm4lMjBiYXJiZXJzaG9wfGVufDF8fHx8MTc2NzI4MzcyOHww&ixlib=rb-4.1.0&q=80&w=1080&utm_source=figma&utm_medium=referral"
        alt="img/png"
      />
    </div>
    <div class="imgContainer">
      <img
        src="https://images.unsplash.com/photo-1547648946-2b1fd7eab923?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3w3Nzg4Nzd8MHwxfHNlYXJjaHwxfHxiYXJiZXIlMjBjdXR0aW5nJTIwaGFpcnxlbnwxfHx8fDE3NjczMzI2MzZ8MA&ixlib=rb-4.1.0&q=80&w=1080&utm_source=figma&utm_medium=referral"
        alt="img/png"
      />
    </div>
  </div>
</template>

<style scoped>
div:not(.imgContainer) {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1rem;
  padding: 2rem;
}

.imgContainer {
  width: 100%;
  height: 300px;
  margin-bottom: 1rem;
  overflow: hidden;
  border-radius: 8px;
}

.imgContainer img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.5s ease;
  cursor: pointer;
}

.imgContainer img:hover {
  transform: scale(1.1);
}
</style>
