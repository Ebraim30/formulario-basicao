<script setup>
import { onMounted, ref } from 'vue';
import Swal from 'sweetalert2';

const navbar = ref(null);
const showMenu = ref(false);

const showAlert = () => {
  Swal.fire({
    title: 'Sessão de Ensino Médio em breve!',
    icon: 'info',
    confirmButtonText: 'OK',
  });
};

onMounted(() => {
  window.onscroll = () => {
    if (window.scrollY === 0) {
      navbar.value.style.backdropFilter = 'blur(10px)';
    } else {
      navbar.value.style.backdropFilter = 'blur(10px)';
    }
  };

  const ensinoMedioLink = document.querySelector('#ensinoMedioLink');

  if (ensinoMedioLink) {
    ensinoMedioLink.addEventListener('click', showAlert);
  }
});
</script>

<template>
  <nav ref="navbar" class="fixed top-0 left-0 w-full z-20 transition duration-200">
    <div class="container flex items-center justify-between h-20">
      <div class="relative z-30 flex items-center gap-2 mb-2 lg:mb-0">
        <img src="../assets/maenatureza/logocemn.png" class="h-16" alt="">
        <a @click="showMenu = false" class="text-white font-medium" href="#home"><h1 class="text-white font-bold text-lg lg:text-2xl">Colégio Mãe<span class="text-secondary"> Natureza</span>
        </h1></a>
      </div>
      <div class="flex lg:hidden items-center gap-2">
        <a href="https://beacons.ai/cemn_" target="_blank">
          <button
            class="relative z-30 px-4 py-2 -mt-1.5 text-sm rounded-full text-white font-medium tracking-wider uppercase bg-secondary w-full lg:w-auto">Contatos</button></a>
        <button @click="showMenu = !showMenu" class="relative z-30 text-white -mt-2 p-2">
          <svg width="18" height="12" viewBox="0 0 18 12" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path
              d="M1 12H17C17.55 12 18 11.55 18 11C18 10.45 17.55 10 17 10H1C0.45 10 0 10.45 0 11C0 11.55 0.45 12 1 12ZM1 7H17C17.55 7 18 6.55 18 6C18 5.45 17.55 5 17 5H1C0.45 5 0 5.45 0 6C0 6.55 0.45 7 1 7ZM0 1C0 1.55 0.45 2 1 2H17C17.55 2 18 1.55 18 1C18 0.45 17.55 0 17 0H1C0.45 0 0 0.45 0 1Z"
              fill="white" />
          </svg>
        </button>
      </div>
      <div class="
  absolute lg:static top-20 inset-x-0
  flex flex-col lg:flex-row items-center gap-5 lg:gap-10
  bg-pink-900 lg:bg-transparent pt-5 pb-10 px-5 lg:p-0
  transition duration-500 lg:duration-200 lg:-translate-y-0
" :class="!showMenu ? 'translate-y-[-150%]' : '-translate-y-0'"
        :style="{ backdropFilter: showMenu ? 'blur(10px)' : 'none' }">
        <a @click="showMenu = false" class="text-white font-medium" href="#educacaoinfantil">EDUCAÇÃO INFANTIL</a>
        <a @click="showMenu = false" class="text-white  font-medium" href="#fun1">ENSINO FUNDAMENTAL I</a>
        <a @click="showMenu = false" class="text-white  font-medium" href="#fun2">ENSINO FUNDAMENTAL II</a>
        <a @click="showMenu = false" class="text-white  font-medium" href="#medio">ENSINO MÉDIO</a>
        <a href="https://beacons.ai/cemn_" target="_blank">
          <button
            class="hidden md:block px-5 py-3 rounded-full text-white font-medium tracking-wider uppercase bg-secondary w-full lg:w-auto">Contatos</button>
        </a>

      </div>
    </div>
  </nav>
</template>