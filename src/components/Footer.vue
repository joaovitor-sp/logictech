<template>
  <div
    class="container-fluid d-flex"
    style="flex-wrap: wrap; gap: 10px; background-color: #871cbf; justify-content: space-around;"
  >
    <div class="topic m-2">
      <div class="topic-header">
        <h4>
          <img
            src="/src/assets/NavBar/logo.png"
            style="max-width: 50px; max-height: 50px"
            alt="Logo"
          />LogicTech
        </h4>
      </div>
      <ul id="social-links">
        <li>
          <a href="#"><i class="fab fa-whatsapp"></i> whatsapp</a>
        </li>
        <li>
          <a href="#"><i class="fab fa-instagram"></i> instagram</a>
        </li>
        <li>
          <a href="#"><i class="fab fa-youtube"></i> youtube</a>
        </li>
        <li>
          <a href="#"><i class="fab fa-twitch"></i> twitch</a>
        </li>
      </ul>
    </div>
    <div class="topic m-3">
      <div class="topic-header">
        <h4>
          Contato
        </h4>
      </div>
      <ul id="social-links">
        <li>
          <a href="(31)43942-0678"><i class="fab fa-whatsapp"></i> (31)43942-0678</a>
        </li>
        <li>
          <a href="(31)43942-0678"><i class="fa-solid fa-phone"></i> (31)43942-0678</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.topic {
    display: flex;
    flex-direction: column;
    justify-content: center;
    border: 1px solid #65daf9;
    border-radius: 10px;
    padding: 20px;
    width: 45%;
}

.topic .topic-header h4 {
  text-align: center;
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
  color: white;
}

#social-links {
    list-style-type: none;
    font-size: 20px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    padding: 0;
}

#social-links i {
    margin-left: 15px;
}

</style>