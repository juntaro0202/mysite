<template>
  <img
    class="MainLogo"
    alt="Main Logo"
    src="/あ.png"
  >
</template>

<style>
.MainLogo {
  height: 180px;
  width: 180px;
  transform: rotateY(560deg);
  animation: turn 3.5s ease-out forwards 1s;
}

@keyframes turn {
  100% {
    transform: rotateY(0deg);
  }
}
</style>
