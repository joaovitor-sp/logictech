<template>
    <nav
      class="navbar navbar-expand-lg navbar-dark px-4 vw-100"
      style="background-color: #871cbf"
    >
      <img
        src="./assets/NavBar/logo.png"
        style="max-width: 50px; max-height: 50px"
        alt="Logo"
      />
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarNavAltMarkup"
        aria-controls="navbarNavAltMarkup"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        <div class="navbar-nav">
          <a class="nav-item nav-link active" href="/">Home</a>
          <a class="nav-item nav-link" href="#">Quem somos?</a>
          <a class="nav-item nav-link" href="/contact">Solicitar serviço</a>
          <a class="nav-item nav-link disabled" href="#"
            ><i class="fab fa-whatsapp"></i
          ></a>
          <a class="nav-item nav-link disabled" href="#"
            ><i class="fab fa-instagram"></i
          ></a>
          <a class="nav-item nav-link disabled" href="#"
            ><i class="fab fa-youtube"></i
          ></a>
          <a class="nav-item nav-link disabled" href="#"
            ><i class="fab fa-twitch"></i
          ></a>
        </div>
      </div>
    </nav>
    <router-view />
</template>

<script>
import { RouterLink, RouterView } from "vue-router";
</script>