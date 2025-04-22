<template>
    <header>
    <nav
      class="navbar navbar-expand-lg navbar-dark px-4"
      style="background-color: #000000"
    >
      <div class="container-fluid">
        <img
          src="/src/assets/NavBar/logo.png"
          style="max-width: 100px; max-height: 50px"
          alt="Logo"
        /> 
          <h3
          class="m-0" 
          style="font-weight: 750; font-size: 30px; font-family: 'Times New Roman', Times, serif; color: white; ">LogicTech</h3>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNavAltMarkup"
          aria-controls="navbarNavAltMarkup"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div
          class="collapse navbar-collapse justify-content-end"
          id="navbarNavAltMarkup"
        >
          <ul class="navbar-nav">
            <li class="nav-item">
              <a class="nav-link" href="/">Home</a>
            </li>
            <!-- TODO: Implemantar nova aba -->
            <!-- <li class="nav-item">
              <a class="nav-link" href="#">Regiões de atendimento</a>
            </li> -->
            <li class="nav-item">
              <a class="nav-link" href="/contact">Solicitar serviço</a>
            </li>
            <li class="nav-item d-flex flex-row">
              <a class="nav-link" href="https://wa.me/31992528746"
                ><i class="fab fa-whatsapp"></i
              ></a>
              <a class="nav-link" href="https://www.instagram.com/_logictech/"
                ><i class="fab fa-instagram"></i
              ></a>
              <a class="nav-link" href="https://www.youtube.com/channel/UCYabfaoYpD2lJaSl_EsWr-Q"
                ><i class="fab fa-youtube"></i
              ></a>
              <a class="nav-link" href="https://www.twitch.tv/logicctech"
                ><i class="fab fa-twitch"></i
              ></a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </header>
</template>

<style scoped>
a.nav-link {
  padding: 4px;
  colo: white;
}
</style>