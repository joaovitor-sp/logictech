<template>
  <div class="container-fluid bg-dark min-vh-100 p-2 contact-page">
    <div class="contact-wrapper">
      <!-- FORMULÁRIO -->
      <form class="contact-form">
        <h2>Entre em contato</h2>

        <div class="form-group">
          <label>Nome</label>
          <input type="text" v-model="nameInput" class="form-control" />
        </div>

        <div class="form-group">
          <label>Email</label>
          <input type="email" v-model="emailInput" class="form-control" />
        </div>

        <div class="form-group">
          <label>Celular</label>
          <input type="text" v-model="phoneNumberInput" class="form-control" />
        </div>

        <div class="form-group">
          <label>Assunto</label>
          <input type="text" v-model="aboutInput" class="form-control" />
        </div>

        <div class="form-group">
          <label>Mensagem</label>
          <textarea
            rows="5"
            v-model="descriptionInput"
            class="form-control"
          ></textarea>
        </div>

        <button class="btn btn-primary" @click.prevent="sendForms">
          Enviar formulário
        </button>

        <p
          v-if="feedbackMessage"
          :class="
            feedbackType === 'success' ? 'feedback-success' : 'feedback-error'
          "
        >
          {{ feedbackMessage }}
        </p>
      </form>

      <!-- INFORMAÇÕES -->
      <div class="contact-info">
        <div class="info-card">
          <i class="fa-solid fa-location-dot"></i>
          <h3>Localidade</h3>
          <span>BH e região de Contagem</span>
        </div>

        <div class="info-card">
          <i class="fa-brands fa-whatsapp"></i>
          <h3>Whatsapp</h3>
          <span>(31) 99252-8746</span>
          <span>(31) 99760-2403</span>
        </div>

        <div class="info-card">
          <i class="fa-regular fa-envelope"></i>
          <h3>Email</h3>
          <span>logictech@gmail.com</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import emailjs from "@emailjs/browser";

const nameInput = ref("");
const emailInput = ref("");
const phoneNumberInput = ref("");
const aboutInput = ref("");
const descriptionInput = ref("");

const feedbackMessage = ref("");
const feedbackType = ref(""); // success | error

function isValidEmail(email) {
  const regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
  return regex.test(email);
}

function validateForm() {
  if (!nameInput.value.trim()) {
    return "Por favor, informe seu nome.";
  }

  if (!emailInput.value.trim()) {
    return "Por favor, informe seu email.";
  }

  if (!isValidEmail(emailInput.value)) {
    return "Por favor, informe um email válido.";
  }

  if (!aboutInput.value.trim()) {
    return "Por favor, informe o assunto.";
  }

  if (!descriptionInput.value.trim()) {
    return "Por favor, escreva sua mensagem.";
  }

  return null;
}

async function sendForms() {
  feedbackMessage.value = "";
  feedbackType.value = "";

  const error = validateForm();
  if (error) {
    feedbackMessage.value = error;
    feedbackType.value = "error";
    return;
  }

  const serviceId = "service_bcxf6ih";
  const templateId = "template_w1h4ban";
  const userId = "kjTfiD2FFsTA0YAk-";

  const templateParams = {
    name: nameInput.value,
    email: emailInput.value,
    phone: phoneNumberInput.value,
    title: aboutInput.value,
    message: descriptionInput.value,
  };

  try {
    await emailjs.send(serviceId, templateId, templateParams, userId);
    feedbackMessage.value =
      "Mensagem enviada com sucesso! Entraremos em contato em breve.";
    feedbackType.value = "success";

    // limpa formulário
    nameInput.value = "";
    emailInput.value = "";
    phoneNumberInput.value = "";
    aboutInput.value = "";
    descriptionInput.value = "";
  } catch (err) {
    console.error(err);
    feedbackMessage.value =
      "Não foi possível enviar a mensagem no momento. Tente novamente mais tarde.";
    feedbackType.value = "error";
  }
}
</script>

<style scoped>
.contact-page {
  min-height: 100vh;
  height: auto;
}

.contact-wrapper {
  display: flex;
  gap: 40px;
  max-width: 1200px;
  margin: 0 auto;
}

/* FORM */
.contact-form {
  flex: 2;
  background: #1e1e1e;
  padding: 30px;
  border-radius: 8px;
}

.contact-form h2 {
  color: white;
  margin-bottom: 20px;
}

.form-group {
  margin-bottom: 15px;
}

.form-group label {
  color: white;
  font-weight: 600;
  margin-bottom: 5px;
  display: block;
}

.form-control {
  background: #9d9d9d;
  border: none;
}

.form-control:focus {
  background: #9d9d9d;
  box-shadow: none;
}

/* FEEDBACK */
.feedback-success {
  color: #28a745;
  font-weight: 600;
}

.feedback-error {
  color: #dc3545;
  font-weight: 600;
}

/* INFO */
.contact-info {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.info-card {
  background: #2a2a2a;
  padding: 20px;
  border-radius: 8px;
  text-align: center;
}

.info-card i {
  font-size: 36px;
  color: #65daf9;
  margin-bottom: 10px;
}

.info-card h3,
.info-card span {
  color: white;
}

/* RESPONSIVO */
@media (max-width: 768px) {
  .contact-wrapper {
    flex-direction: column;
  }
}
</style>