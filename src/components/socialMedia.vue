<template>
 <div class="social-links">
    <a href="https://github.com/JoaRampa" target="_blank" rel="noopener noreferrer" aria-label="GitHub">
      <img src="../assets/github.png" class="social-icon" alt="GitHub">
    </a>
    <a href="https://linkedin.com/in/tu-usuario" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn">
      <img src="../assets/in.png" class="social-icon" alt="LinkedIn">
    </a>
    <a href="https://linkedin.com/in/tu-usuario" target="_blank" rel="noopener noreferrer" aria-label="Instagram">
      <img src="../assets/ig.png" class="social-icon" alt="Instagram">
    </a>
    <a href="https://linkedin.com/in/tu-usuario" target="_blank" rel="noopener noreferrer" aria-label="Mail">
      <img src="../assets/mail.png" class="social-icon" alt="Mail">
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
  width: 1.5rem;
  height: 1.5rem;
  transition: all 0.3s ease;
  opacity: 0.7;
}

.social-icon:hover {
  opacity: 1;
  transform: translateY(-1px);
  filter: brightness(250%);
}
</style>