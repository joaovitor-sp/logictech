<template>
    <header>
    <nav
      class="navbar navbar-expand-lg navbar-dark px-4 vw-100"
      style="background-color: #871cbf"
    >
      <div class="container-fluid">
        <img
          src="/src/assets/NavBar/logo.png"
          style="max-width: 50px; max-height: 50px"
          alt="Logo"
        />
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
              <a class="nav-link active" href="/">Home</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Quem somos?</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="/contact">Solicitar serviço</a>
            </li>
            <li class="nav-item d-flex flex-row">
              <a class="nav-link disabled" href="#"
                ><i class="fab fa-whatsapp"></i
              ></a>
              <a class="nav-link disabled" href="#"
                ><i class="fab fa-instagram"></i
              ></a>
              <a class="nav-link disabled" href="#"
                ><i class="fab fa-youtube"></i
              ></a>
              <a class="nav-link disabled" href="#"
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
}
</style>