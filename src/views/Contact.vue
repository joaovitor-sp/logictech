<template>
  <div id="content-page-contact-container" class="container-fluid p-0 m-0">
    <div id="content-page-contact-row" class="p-0 m-0 w-100 h-100">
      <div class="col p-5" style="background-color: dimgray">
        <div class="row pt-4">
          <label class="col-1 col-form-label">Nome:</label>
          <input
            type="text"
            class="col-10 form-control"
            id="name"
            placeholder="Digite seu nome"
          />
        </div>
        <div class="row pt-4">
          <label for="email" class="col-1 col-form-label">Email:</label>
          <input
            type="text"
            class="col-10 form-control"
            id="email"
            placeholder="Digite seu email"
          />
        </div>
        <div class="row pt-4">
          <label for="about" class="col-1 col-form-label">Assunto:</label>
          <input
            type="text"
            class="col-10 form-control"
            id="about"
            placeholder="Digite o assunto"
          />
        </div>
        <div class="row pt-4">
          <label class="col-form-label">Mensagem:</label>
        </div>
        <div class="row pt-4" style="padding-right: 10%;">
            <textarea
              type="text"
              class="form-control"
              id="description"
              rows="5"
            ></textarea>
        </div>
      </div>
      <div
        class="flex-wrap justify-items-stretch"
        id="informations"
        style="background-color: black;"
      >
        <div
          class="card-information col d-flex flex-column"
          id="location"
          style="align-items: center; justify-content: center"
        >
          <i class="fa-solid fa-location-dot"></i>
          <span>Localidade</span>
        </div>
        <div
          class="card-information col d-flex flex-column"
          id="whatsapp"
          style="align-items: center; justify-content: center;"
        >
          <i class="fa-brands fa-whatsapp"></i>
          <span>Whatsapp</span>
        </div>
        <div
          class="card-information col d-flex flex-column"
          id="email"
          style="align-items: center; justify-content: center"
        >
          <i class="fa-regular fa-envelope"></i>
          <span>Email de Contato</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
#content-page-contact-container {
  flex: 1;
}
#content-page-contact-row {
  display: flex;
  flex-direction: column;
}
#informations {
  display: flex;
  flex-direction: row;
}
#informations div span {
  text-align: center;
}
i {
  font-size: 40px;
  color: white;
}
span {
  font-size: 20px;
  color: white;
}
input {
  background-color: rgb(157, 157, 157);
}

textarea {
  background-color: rgb(157, 157, 157);
}

@media (max-width: 767px) {
  #location, #whatsapp {
    width: 50%;
  }
}
@media (min-width: 768px) {
  #content-page-contact-row {
    display: flex;
    flex-direction: row;
  }
  #informations {
    display: flex;
    flex-direction: column;
  }
  i {
    font-size: 70px;
    color: white;
  }
  span {
    font-size: 30px;
    color: white;
  }
  input {
    background-color: rgb(157, 157, 157); /* Fundo amarelo claro */
  }

  textarea {
    background-color: rgb(157, 157, 157); /* Fundo Verde claro */
  }
  input#name,
  input#about,
  input#email {
    width: 50vw;
  }
}
</style>

<script>
export default {
  name: "Contact",
};
</script>
