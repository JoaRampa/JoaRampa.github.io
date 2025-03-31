<template>
 <div class="social-links">
    <a href="https://github.com/JoaRampa" target="_blank" rel="noopener noreferrer" aria-label="GitHub">
      <img src="../assets/github.png" class="social-icon" alt="GitHub">
    </a>
    <a href="https://linkedin.com/in/tu-usuario" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn">
      <svg class="social-icon">...</svg>
    </a>
  </div>
</template>

<style>
.social-links {
  display: flex;
  align-items: center;
  gap: 1.5rem;
  margin-top: 1rem;
}

.social-icon {
  width: 2.5rem;
  height: 2.5rem;
  transition: all 0.3s ease;
}

.social-icon:hover {
  transform: translateY(-1px);
  filter: brightness(150%) saturate(100%);
}
</style>