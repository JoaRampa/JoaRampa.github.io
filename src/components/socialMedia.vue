<template>
 <div class="social-links">
    <a href="https://github.com/JoaRampa" target="_blank" rel="noopener noreferrer" aria-label="GitHub">
      <img src="../assets/github.png" class="social-icon" alt="GitHub">
    </a>
    <a href="https://www.linkedin.com/in/joaquin-rampa-5b2861243/" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn">
      <img src="../assets/in.png" class="social-icon" alt="LinkedIn">
    </a>
    <a href="https://www.instagram.com/joaarampa/" target="_blank" rel="noopener noreferrer" aria-label="Instagram">
      <img src="../assets/ig.png" class="social-icon" alt="Instagram">
    </a>
    <a href="mailto:rampajoa@gmail.com" target="_blank" rel="noopener noreferrer" aria-label="Mail">
      <img src="../assets/mail.png" class="social-icon" alt="Mail">
    </a>
    <a href="https://profile.indeed.com/?hl=it_IT&co=IT&from=gnav-homepage" target="_blank" rel="noopener noreferrer" aria-label="Mail">
      <img src="../assets/indeed.png" class="social-icon" alt="Indeed" style="width: 2rem; height: 2.2rem;">
    </a>
  </div>
</template>

<style>
.social-links {
  display: flex;
  align-items: center;
  gap: 1.5rem;
  margin-top: 12rem;
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