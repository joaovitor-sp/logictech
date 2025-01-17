<template>
    <div class="container-fluid">
      <div id="mainSlider" class="carousel slide" data-bs-ride="carousel">
        <ol class="carousel-indicators">
          <li data-bs-target="#mainSlider" data-bs-slide-to="0" class="active"></li>
          <li data-bs-target="#mainSlider" data-bs-slide-to="1"></li>
          <li data-bs-target="#mainSlider" data-bs-slide-to="2"></li>
        </ol>
        <div class="carousel-inner">
          <div class="carousel-item active">
            <img src="/src/assets/Home/slide-0.jpg" alt="Apresentação" class="d-block w-100">
            <div class="carousel-caption d-md-block">
              <h2>Como podemos te ajudar?</h2>
              <p>Conte conosco para te ajudar a com seu seu computador!</p>
              <a href="" class="main-btn">Ver Serviços</a>
            </div>
          </div>
          <div class="carousel-item">
            <img src="/src/assets/Home/slide-1.jpg" alt="Redes Sociais" class="d-block w-100">
            <div class="carousel-caption d-md-block">
              <h2>Onde atendemos?</h2>
              <p>Veja se onde atendemos para te ajudarmos da melhor forma.</p>
              <a href="" class="main-btn">Ver mapa</a>
            </div>
          </div>
          <div class="carousel-item">
            <img src="/src/assets/Home/slide-2.jpg" alt="Solicitação de serviço" class="d-block w-100">
            <div class="carousel-caption d-md-block">
              <h2>Solicitar serviço</h2>
              <p>Clique no botão abaixo e envie sua solicitação.</p>
              <a href="" class="main-btn">Solicitar serviço</a>
            </div>
          </div>
        </div>
        <a href="#mainSlider" class="carousel-control-prev" role="button" data-bs-slide="prev">
          <span class="carousel-control-prev-icon" area-hidden="true"></span>
          <span class="sr-only">Previous</span>
        </a>
        <a href="#mainSlider" class="carousel-control-next" role="button" data-bs-slide="next">
          <span class="carousel-control-next-icon" area-hidden="true"></span>
          <span class="sr-only">Next</span>
        </a>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Home'
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
  }

  #mainSlider .carousel-inner, #mainSlider .carousel-item {
    height: 90vh;
  }

  #mainSlider .carousel-caption {
    top:30%;
  }

  #mainSlider .carousel-caption h2 {
    font-size: 50px;
    margin-bottom: 30px;
  }
  #mainSlider .carousel-caption p {
    font-size: 22px;
    font-weight: 300;
    margin-bottom: 100px;
    color: #FFF;
  }

  .main-btn {
    text-decoration: none;
    background-color: #65DAF9;
    color: #FFF;
    text-transform: uppercase;
    width: 200px;
    height: 60px;
    padding: 10px 20px;
    border-radius: 30px;
    border: 3px solid transparent;
    transition: .5s;
  }

  .main-btn:hover {
    text-decoration: none;
    color: #FFF;
    background-color: transparent;
    border-color: #65DAF9;
  }

  .carousel-indicators .active {
    background-color: #65DAF9;
  }

  .carousel-item img {
    filter: brightness(0.6) contrast(1.2);
}

/* Responsive */
@media(max-width: 768px) {

  .container {
    padding: 20px 0;
  }

  /* slider */
  #mainSlider .carousel-inner, #mainSlider .carousel-item {
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

@media(max-width: 425px){

  /* slider */
  #mainSlider .carousel-caption{
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