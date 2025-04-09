<template>
  <div id="content-page-contact-container" class="container-fluid p-0 m-0">
    <div id="content-page-contact-row" class="p-0 m-0 w-100 h-100">
      <div class="col p-5" style="background-color: black">
        <div class="row pt-4">
          <label class="col-1 col-form-label">Nome:</label>
          <input type="text" class="col-10 form-control" id="name" placeholder="Digite seu nome" v-model="nameInput" />
        </div>
        <div class="row pt-4">
          <label for="email" class="col-1 col-form-label">Email:</label>
          <input type="text" class="col-10 form-control" id="email" placeholder="Digite seu email"
            v-model="emailInput" />
        </div>
        <div class="row pt-4">
          <label for="phoneNumber" class="col-1 col-form-label">Celular:</label>
          <input type="text" class="col-10 form-control" id="phoneNumber" placeholder="Digite seu whatsapp"
            v-model="phoneNumberInput" />
        </div>
        <div class="row pt-4">
          <label for="about" class="col-1 col-form-label">Assunto:</label>
          <input type="text" class="col-10 form-control" id="about" placeholder="Digite o assunto"
            v-model="aboutInput" />
        </div>
        <div class="row pt-4">
          <label class="col-form-label">Mensagem:</label>
        </div>
        <div class="row pt-4" style="padding-right: 10%;">
          <textarea type="text" class="form-control" id="description" rows="5" v-model="descriptionInput"></textarea>
        </div>
        <div class="row pt-4 justify-content-end" style="padding-right: 10%;">
          <button type="button" @click="sendForms" class="btn btn-primary" style="width: auto;">Enviar
            Formulário</button>
        </div>
        <div class="row pt-4 justify-content-end" style="padding-right: 10%;">
          <h3 id="feedBackSend"></h3>
        </div>
      </div>
      <div class="flex-wrap justify-items-stretch" id="informations" style="background-color: black;">
        <div class="card-information col d-flex flex-column" id="location"
          style="align-items: center; justify-content: center">
          <i class="fa-solid fa-location-dot"></i>
          <h3>Localidade</h3>
          <span>Atendemos por visita Técnica<br>
            em BH e região de Contagem</span>

        </div>
        <div class="card-information col d-flex flex-column" id="whatsapp"
          style="align-items: center; justify-content: center;">
          <i class="fa-brands fa-whatsapp"></i>
          <h3>Whatsapp:</h3>
          <span>(31)99252-8746</span>
          <span>(31)99760-2403</span>
        </div>
        <div class="card-information col d-flex flex-column" id="email"
          style="align-items: center; justify-content: center">
          <i class="fa-regular fa-envelope"></i>
          <h3>Email de Contato:</h3>
          <span>logictech@gmail.com</span>
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
  padding: 10px;
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

h3 {
  font-size: 20px;
  color: white;
}

span {
  font-size: 15px;
  color: white;
}

input {
  background-color: rgb(157, 157, 157);
}

textarea {
  background-color: rgb(157, 157, 157);
}

.col-form-label {
  color: white;
  font-size: 20px;
  font-weight: 600;
}

@media (max-width: 767px) {

  #location,
  #whatsapp {
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
    padding: 10px;
  }

  i {
    font-size: 40px;
    color: white;
  }

  h3 {
    font-size: 30px;
    color: white;
  }

  span {
    font-size: 20px;
    color: white;
  }

  input {
    background-color: rgb(157, 157, 157);
    /* Fundo amarelo claro */
  }

  input:focus {
    background-color: rgb(157, 157, 157);
    /* Fundo amarelo claro */
  }

  textarea {
    background-color: rgb(157, 157, 157);
    /* Fundo Verde claro */
  }

  textarea:focus {
    background-color: rgb(157, 157, 157);
    /* Fundo Verde claro */
  }

  input#name,
  input#about,
  input#phoneNumber,
  input#email {
    width: 50vw;
  }
}
</style>

<script>
import emailjs from '@emailjs/browser';

export default {
  name: "Contact",
  data() {
    return {
      nameInput: '',
      emailInput: '',
      phoneNumberInput: '',
      aboutInput: '',
      descriptionInput: ''
    }
  },
  methods: {
    sendForms() {
      const serviceId = 'service_ckzzscc';
      const templateId = 'template_w1h4ban';
      const userId = 'kjTfiD2FFsTA0YAk-';

      const templateParams = {
        name: this.nameInput,
        email: this.emailInput,
        phone: this.phoneNumberInput,
        title: this.aboutInput,
        message: this.descriptionInput
      };
      console.log("está na função");
      const feedbackSend = document.getElementById('feedBackSend');
      emailjs.send(serviceId, templateId, templateParams, userId)
        .then((response) => {
          console.log('E-mail enviado com sucesso!', response);
          feedbackSend.textContent = 'E-mail enviado com sucesso!';
          feedbackSend.style.color = 'green'
          alert('E-mail enviado com sucesso!');
        })
        .catch((error) => {
          console.error('Erro ao enviar o e-mail:', error);
          feedbackSend.textContent = 'Erro ao enviar o e-mail!';
          feedbackSend.style.color = 'red'
          alert('Erro ao enviar o e-mail.');
        });
    }
  }
};
</script>
