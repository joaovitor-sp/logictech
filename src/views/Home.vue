<template>
  <div class="container-fluid" style="background-color: black">
    <div id="mainSlider" class="carousel slide" data-bs-ride="carousel">
      <ol class="carousel-indicators">
        <li
          data-bs-target="#mainSlider"
          data-bs-slide-to="0"
          class="active"
        ></li>
        <li data-bs-target="#mainSlider" data-bs-slide-to="1"></li>
        <li data-bs-target="#mainSlider" data-bs-slide-to="2"></li>
      </ol>
      <div class="carousel-inner">
        <div class="carousel-item active">
          <img
            src="/src/assets/Home/slide-0.jpg"
            alt="Apresentação"
            class="d-block w-100"
          />
          <div class="carousel-caption d-md-block">
            <h2>Como podemos te ajudar?</h2>
            <p>Conte conosco para te ajudar a com seu seu computador!</p>
            <a href="" class="main-btn">Ver Serviços</a>
          </div>
        </div>
        <div class="carousel-item">
          <img
            src="/src/assets/Home/slide-1.jpg"
            alt="Redes Sociais"
            class="d-block w-100"
          />
          <div class="carousel-caption d-md-block">
            <h2>Onde atendemos?</h2>
            <p>Veja se onde atendemos para te ajudarmos da melhor forma.</p>
            <a href="" class="main-btn">Ver mapa</a>
          </div>
        </div>
        <div class="carousel-item">
          <img
            src="/src/assets/Home/slide-2.jpg"
            alt="Solicitação de serviço"
            class="d-block w-100"
          />
          <div class="carousel-caption d-md-block">
            <h2>Solicitar serviço</h2>
            <p>Clique no botão abaixo e envie sua solicitação.</p>
            <a href="" class="main-btn">Solicitar serviço</a>
          </div>
        </div>
      </div>
      <a
        href="#mainSlider"
        class="carousel-control-prev"
        role="button"
        data-bs-slide="prev"
      >
        <span class="carousel-control-prev-icon" area-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a
        href="#mainSlider"
        class="carousel-control-next"
        role="button"
        data-bs-slide="next"
      >
        <span class="carousel-control-next-icon" area-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>
    </div>
    <div id="services" class="col">
      <div
        class="service"
      >
        <img
          src="/src/assets/Home/manutencao.jpeg"
          alt="manutenção"
        />
        <div class="service-information">
          <h3>Montagem de Computadores</h3>
          <span>Comprou seu PC Gamer e não consegue montar?<br>
            Montamos PCs Gamers em domicílio, <br>montagem completa e otimizada<br>
            com instalação de sistema operacional e configuração<br>
            para o melhor desempenho. </span>
        </div>
      </div>
      <div class="service">
        <img
          src="/src/assets/Home/montagem.jpg"
          alt="montagem"
        />
        <div class="service-information">
          <h3>Manutenção e Otimização</h3>
          <span>Otimizamos o desempenho do seu PC <br>
            para aproveitar mais o potêncial do seu computador,<br> 
            solução de problemas e manutenção.
          </span>
        </div>
      </div>
    </div>
    <h2 style="display: flex; justify-content: center; color: white;"> E entre outros...</h2>
    <div id="service-list" class="p-0 m-5" style="display: flex; flex-wrap: wrap; gap: 20px; justify-content: center; color: white;">
        <span><i class="fa-regular fa-circle-check"></i>Diagnóstico e correção de defeitos</span>
        <span><i class="fa-regular fa-circle-check"></i>Backups e recuperação de dados</span>
        <span><i class="fa-regular fa-circle-check"></i>Correção de inicialização</span>
        <span><i class="fa-regular fa-circle-check"></i>Limpeza interna</span>
        <span><i class="fa-regular fa-circle-check"></i>Upgrades e otimização</span>
        <span><i class="fa-regular fa-circle-check"></i>Correção de tela azul</span>
        <span><i class="fa-regular fa-circle-check"></i>Instalação de computadores novos</span>
        <span><i class="fa-regular fa-circle-check"></i>Remoção de vírus e spywares</span>
        <span><i class="fa-regular fa-circle-check"></i>Instalação e remoção de softwares</span>
        <span><i class="fa-regular fa-circle-check"></i>Configuração de emails e contas online</span>
        <span><i class="fa-regular fa-circle-check"></i>Formatação e reinstalação do sistema operacional</span>
    </div>
  </div>
</template>
  
  <script>
export default {
  name: "Home",
};
</script>
  
  <style scoped>
.home-container {
  display: flex;
  flex-direction: column;
  align-items: center; /* Centraliza horizontalmente */
  padding: 20px;
  background-color: #f0f0f0; /* Um fundo cinza claro */
  border-radius: 8px; /* Bordas arredondadas */
}

h1 {
  color: #333; /* Cor do título */
  margin-bottom: 10px;
}

/* Slider */
.container-fluid {
  padding: 0;
  margin: 0;
}

#mainSlider .carousel-inner,
#mainSlider .carousel-item {
  height: 90vh;
}

#mainSlider .carousel-caption {
  top: 30%;
}

#mainSlider .carousel-caption h2 {
  font-size: 50px;
  margin-bottom: 30px;
}
#mainSlider .carousel-caption p {
  font-size: 22px;
  font-weight: 300;
  margin-bottom: 100px;
  color: #fff;
}

.main-btn {
  text-decoration: none;
  background-color: #65daf9;
  color: #fff;
  text-transform: uppercase;
  width: 200px;
  height: 60px;
  padding: 10px 20px;
  border-radius: 30px;
  border: 3px solid transparent;
  transition: 0.5s;
}

.main-btn:hover {
  text-decoration: none;
  color: #fff;
  background-color: transparent;
  border-color: #65daf9;
}

.carousel-indicators .active {
  background-color: #65daf9;
}

.carousel-item img {
  filter: brightness(0.6) contrast(1.2);
}

.services {
  width: 100%;
  margin-top: 30px;
}

.service {
  display: inline-flex;
  flex-wrap: wrap;
  gap: 10px;
  margin: 10px;
}

.service img {
  width: 280px;
  height: 280px;
  margin: 16px;
}

.service-information {
  color: white;
  margin: 30px;
  margin-right: 10px;
}

.service-information span {
  font-weight: 300;
}

#service-list span {
  font-size: 20px;
}

#service-list span i {
  margin-right: 10px;
  color: #65daf9;
}

/* Responsive */
@media (max-width: 768px) {
  .container {
    padding: 20px 0;
  }

  /* slider */
  #mainSlider .carousel-inner,
  #mainSlider .carousel-item {
    height: auto;
  }

  #mainSlider .carousel-caption h2 {
    font-size: 24px;
  }

  #mainSlider .carousel-caption p {
    font-size: 12px;
    margin-bottom: 35px;
  }

  .carousel-caption {
    left: 10%;
    right: 10%;
  }
}

@media (max-width: 425px) {
  /* slider */
  #mainSlider .carousel-caption {
    top: 5%;
    align-content: center;
  }

  #mainSlider .carousel-caption h2 {
    font-size: 18px;
    margin-bottom: 40px;
  }

  #mainSlider .carousel-caption p {
    display: none;
  }
}
</style>