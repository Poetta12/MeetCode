<script setup>
import { ref } from 'vue';

const instaUrl = ref('https://www.instagram.com/poettawds');
const whatsappUrl = ref('https://wa.me/33753812381');
const telegramUrl = ref('https://t.me/Poettawds');

// Fonction pour gérer le clic sur le QR code
function handleQrClick(url) {
  window.open(url, '_blank');
}
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <h3>
      Je ne voulais pas te déranger, mais tu me plaît. Ça serait cool de faire connaissance 😇. Je te laisse mon contact 😊.
    </h3>
    <p>
      Pour lui répondre:
    </p>
    <div id="insta">
      <img src="/QR/poettawds_qr.png" alt="insta QR" @click="handleQrClick(instaUrl)">
    </div>
    <div id="whatsapp">
      <img src="/QR/whatsapp_qr.png" alt="whatsapp QR" @click="handleQrClick(whatsappUrl)">
    </div>
    <div id="telegram">
      <img src="/QR/telegram_qr.png" alt="telegram QR"  @click="handleQrClick(telegramUrl)">
    </div>
  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');

img {
  max-width: 100%;
  border-radius: 20px;
  cursor: pointer; /* Ajoute un curseur pointer pour indiquer que l'image est cliquable */
}

h1 {
  font-weight: 400;
  font-size: 1.5rem;
  position: relative;
  top: -10px;
  color: whitesmoke;
}

h3 {
  font-size: 1rem;
  color: #333;
  background: whitesmoke;
  padding: 10px;
  border-radius: 10px;
  margin-bottom: 20px;
}

.greetings {
  font-family: 'Poppins', sans-serif;
}

.greetings h1 {
  text-align: center;
}

.greetings h3 {
  text-align: justify;
}

.greetings div {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 30px;
}

.greetings > p {
  text-align: center;
  margin-bottom: 30px;
}

.greetings div p {
  font-size: 2rem;
}

.greetings div img {
  width: 50%;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
