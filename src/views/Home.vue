<template>
  <div class="container-fluid bg-dark">
    <HomeCarousel />
    <div id="services" class="services">
      <div v-for="service in services" :key="service.title" class="service">
        <img :src="service.image" :alt="service.title" />
        <div class="service-information">
          <h3>{{ service.title }}</h3>
          <p>{{ service.description }}</p>
        </div>
      </div>
    </div>

    <h2 class="more-services">E entre outros...</h2>

    <div id="service-list" class="service-list">
      <span v-for="item in serviceList" :key="item">
        <i class="fa-regular fa-circle-check"></i>
        {{ item }}
      </span>
    </div>
  </div>
</template>
  
  <script setup>
import HomeCarousel from "../components/home/HomeCarousel.vue";

const services = [
  {
    title: "Montagem de Computadores",
    image: new URL("@/assets/Home/manutenção.jpg", import.meta.url),
    description: `
      Adquiriu seu PC Gamer e está com dificuldades para montá-lo?
      Oferecemos serviço de montagem profissional em domicílio,
      com instalação completa do sistema operacional,
      configurações otimizadas e ajustes para garantir
      o máximo desempenho do seu equipamento.
    `,
  },
  {
    title: "Manutenção e Otimização",
    image: new URL("@/assets/Home/montagem.jpg", import.meta.url),
    description: `
      Realizamos a manutenção completa e a otimização
      do desempenho do seu computador,
      solucionando problemas e garantindo que você
      aproveite ao máximo o potencial da sua máquina.
    `,
  },
];

const serviceList = [
  "Diagnóstico e correção de defeitos",
  "Backups e recuperação de dados",
  "Correção de inicialização",
  "Limpeza interna",
  "Upgrades e otimização",
  "Correção de tela azul",
  "Instalação de computadores novos",
  "Remoção de vírus e spywares",
  "Instalação e remoção de softwares",
  "Configuração de emails e contas online",
  "Formatação e reinstalação do sistema operacional",
];
</script>
  
<style scoped>
/* Container geral */
.container-fluid {
  padding: 0;
  margin: 0;
}

/* ===== SEÇÃO DE SERVIÇOS ===== */
.services {
  display: flex;
  flex-direction: column;
  gap: 40px;
  padding: 60px 5%;
}

/* Card de serviço */
.service {
  display: flex;
  align-items: center;
  gap: 40px;
}

/* Alterna imagem */
.service:nth-child(even) {
  flex-direction: row-reverse;
}

/* Imagem do serviço */
.service img {
  width: 480px;
  max-width: 100%;
  height: auto;
  border-radius: 12px;
}

/* Texto do serviço */
.service-information {
  max-width: 520px;
  color: #fff;
}

.service-information h3 {
  font-size: 28px;
  margin-bottom: 16px;
}

.service-information p {
  font-size: 16px;
  line-height: 1.6;
  font-weight: 300;
}

/* ===== TÍTULO "E ENTRE OUTROS" ===== */
.more-services {
  text-align: center;
  color: #fff;
  margin: 60px 0 30px;
  font-size: 28px;
}

/* ===== LISTA DE SERVIÇOS ===== */
.service-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 20px 40px;
  padding: 0 5% 80px;
  color: #fff;
}

.service-list span {
  font-size: 18px;
  display: flex;
  align-items: center;
  gap: 10px;
}

.service-list i {
  color: #65daf9;
  font-size: 20px;
}

/* ===== RESPONSIVO ===== */
@media (max-width: 992px) {
  .service {
    flex-direction: column;
    text-align: center;
  }

  .service:nth-child(even) {
    flex-direction: column;
  }

  .service img {
    width: 100%;
    max-width: 520px;
  }

  .service-information {
    max-width: 100%;
  }
}
</style>