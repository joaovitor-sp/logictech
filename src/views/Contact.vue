<template>
  <div class="row vw-100 p-0 m-0 d-flex flex-grow-1">
    <div
      class="col-3 d-flex flex-column flex-wrap justify-items-stretch"
      style="background-color: black"
    >
      <div class="col d-flex flex-column" style="height: 40%; align-items: center; justify-content: center;">
        <i class="fa-solid fa-location-dot"></i>
        <span>Localidade</span>
      </div>
      <div class="col d-flex flex-column" style="height: 40%;  align-items: center; justify-content: center;">
        <i class="fa-regular fa-envelope"></i>
        <span>Email de Contato</span>
      </div>
      <div class="col d-flex flex-column" style="height: 40%;  align-items: center; justify-content: center;">
        <i class="fa-brands fa-whatsapp"></i>
        <span>Whatsapp</span>
      </div>
    </div>
    <div
      class="col-9 
      d-flex 
      flex-column 
      flex-wrap
      align-items-around 
      justifi-content-around 
      align-content-around 
      p-5"
      style="background-color: dimgray"
    >
      <div class="mb-3 row pt-4">
        <label for="name" class="col-2 col-md-2 col-form-label">Nome:</label>
        <div class="col-10 col-md-10">
          <input
            type="text"
            class="form-control"
            style="width: 500px"
            id="name"
            placeholder="Digite seu nome"
          />
        </div>
      </div>
      <div class="mb-3 row pt-4">
        <label for="name" class="col-2 col-md-2 col-form-label">Email:</label>
        <div class="col-10 col-md-10">
          <input
            type="text"
            class="form-control"
            style="width: 500px"
            id="name"
            placeholder="Digite seu email"
          />
        </div>
      </div>
      <div class="mb-3 row pt-4">
        <label for="name" class="col-2 col-md-2 col-form-label">Assunto:</label>
        <div class="col-10 col-md-10">
          <input
            type="text"
            class="form-control"
            style="width: 500px"
            id="name"
            placeholder="Digite o assunto"
          />
        </div>
      </div>
      <div class="mb-3 col pt-4">
        <label for="name" class="col col-md-2 col-form-label">Mensagem:</label>
        <div class="col col-md-10">
          <textarea
            type="text"
            class="form-control"
            id="name"
            rows="5"
          ></textarea>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
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
    background-color: rgb(157, 157, 157)  ; /* Fundo Verde claro */
}
</style>

<script>
export default {
  name: "Contact",
};
</script>
