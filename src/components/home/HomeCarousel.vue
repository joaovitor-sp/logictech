<template>
  <div id="mainSlider" class="carousel slide" data-bs-ride="carousel">
    <ol class="carousel-indicators">
      <li
        v-for="(slide, index) in slides"
        :key="index"
        data-bs-target="#mainSlider"
        :data-bs-slide-to="index"
        :class="{ active: index === 0 }"
      />
    </ol>

    <div class="carousel-inner">
      <button
        class="carousel-control-prev"
        type="button"
        data-bs-target="#mainSlider"
        data-bs-slide="prev"
      >
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
      </button>

      <button
        class="carousel-control-next"
        type="button"
        data-bs-target="#mainSlider"
        data-bs-slide="next"
      >
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>

      <div
        v-for="(slide, index) in slides"
        :key="slide.title"
        class="carousel-item"
        :class="{ active: index === 0 }"
      >
        <img :src="slide.image" :alt="slide.title" class="d-block w-100" />

        <div class="carousel-caption d-md-block">
          <h2>{{ slide.title }}</h2>
          <p>{{ slide.text }}</p>

          <RouterLink v-if="slide.link" :to="slide.link" class="main-btn">
            {{ slide.button }}
          </RouterLink>

          <a v-else class="main-btn" @click="scrollToBottom">
            {{ slide.button }}
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const slides = [
  {
    title: "Como podemos te ajudar?",
    text: "Conte conosco para te ajudar com seu computador!",
    image: new URL("@/assets/Home/slide-0.jpg", import.meta.url),
    button: "Ver Serviços",
  },
  {
    title: "Solicitar serviço",
    text: "Clique no botão abaixo e envie sua solicitação.",
    image: new URL("@/assets/Home/slide-2.jpg", import.meta.url),
    button: "Solicitar serviço",
    link: "/contact",
  },
];

function scrollToBottom() {
  const target = document.getElementById('services')

  if (!target) return

  target.scrollIntoView({
    top: target.scrollHeight,
    behavior: 'smooth'
  })
}
</script>

<style scoped>
/* Slider */
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
