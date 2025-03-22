<script setup>
import MySwiper from "./MySwiper.vue"
</script>

<template>
  <section id="home" class="grid place-items-center mt-20 md:mt-10 overflow-hidden">
    <div class="grid grid-flow-row-dense grid-cols-1 lg:grid-cols-2 items-end gap-10 lg:gap-16 w-full px-0 lg:px-10">
      <div class="text-5xl md:text-6xl font-bold text-white w-full pb-20 order-2 lg:order-1">
        <div class="m-10"></div>
        <div class="flex items-center gap-3">
          <h2>COLÉGIO</h2>
          <img class="h-20" src="../assets/maenatureza/logocemn.png" alt="head1-img">
        </div>
        <h2 class="text-4xl md:text-5xl">MÃE NATUREZA!!</h2>
        <p class="pt-5 text-lg font-normal">O Centro Educacional Mae Natureza (CEMN) é uma instituição fundamentada em
          perseverança, fé e dedicação, centrada nos valores do amor. Priorizando Educação, Inclusão Social, Princípios
          Cristãos e Sustentabilidade, sua missão é proporcionar uma educação de qualidade, baseada em princípios
          cristãos, estimulando a inteligência emocional e formação artística, cultural e social. Buscando a
          ressignificação da aprendizagem de forma inovadora, o CEMN utiliza metodologias como STEAM, Ron Clark Academy,
          Reggio Emilia, Maria Montessori e Pedagogia Waldorf. Com valores ancorados em Deus e pilares do projéto caráter
          conta,
          como
          sinceridade e responsabilidade, a instituição promove o protagonismo do aluno, desenvolvendo competências
          socioemocionais e incentivando práticas como empreendedorismo e pesquisa científica. Apostando na formação de
          valores, esporte e cultura, o CEMN compromete-se a evoluir seus educandos por meio de métodos dinâmicos e
          tecnológicos, promovendo o hábito do estudo diário.
        </p>
      </div>
      <div class="w-full h-full order-1 lg:order-2">
        <MySwiper />
      </div>
    </div>
  </section>
</template>