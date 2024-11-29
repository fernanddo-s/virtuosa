<template>
  <div :class="['landing-page', { 'dark-mode': isDarkMode }]">
    <header>
      <button @click="toggleDarkMode" class="toggle-button">
        {{ isDarkMode ? '☀️ Claro' : '🌙 Escuro' }}
      </button>
      <img src="@/assets/logo-vt.png" alt="Logo da Loja" class="logo" />
    </header>

    <section class="info-section">
      <h1>{{ lojaNome }}</h1>
      <p class="description">{{ descricaoLoja }}</p>
      <p>🌻 Tudo o que uma mulher precisa em um só lugar!</p>
      <p>📍 Rua Horácio Oliveira, 107 - Lagoa do Carneiro</p>
      <p>🌟 Beleza Feminina, Cuidado e Estilo</p>
      <br />
      <p>{{ contatoLoja }}</p>

      <!-- Links para Redes Sociais -->
      <div class="social-links">
        <a :href="socialLinks.instagram" target="_blank">
          <img
            src="https://img.icons8.com/ios-glyphs/30/000000/instagram-new.png"
            alt="Instagram"
          />
        </a>
        <a :href="socialLinks.whatsapp" target="_blank">
          <img src="https://img.icons8.com/ios-filled/30/000000/whatsapp.png" alt="WhatsApp" />
        </a>
      </div>
    </section>

    <footer>
      <p>&copy; 2024 {{ lojaNome }} - Todos os direitos reservados.</p>
    </footer>
  </div>
</template>


<script setup>
import { ref } from 'vue';

const lojaNome = 'Virtuosa';
const descricaoLoja = 'Bem-vindos à Virtuosa! Oferecemos produtos de alta qualidade diretamente para você.';
const contatoLoja = 'Entre em contato:';
const socialLinks = {
  instagram: 'https://www.instagram.com/virtuosa_bf/',
  whatsapp: 'https://wa.me/558899516865',
};

const isDarkMode = ref(false);

const toggleDarkMode = () => {
  isDarkMode.value = !isDarkMode.value;
};
</script>



<style scoped>
/* Estilo padrão (modo claro) */
.landing-page {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  height: 100vh;
  background-color: #f4f4f4;
  font-family: 'Arial', sans-serif;
  color: #333;
}

.description {
  margin: 0 20px 20px 20px;
}

.logo {
  max-width: 200px;
  margin-bottom: 20px;
}

.info-section {
  margin: 20px 0;
}

h1 {
  font-size: 2.5em;
  color: #333;
}

p {
  font-size: 1.2em;
  color: #666;
}

.social-links {
  margin-top: 20px;
}

.social-links a {
  margin: 0 10px;
  text-decoration: none;
}

.social-links img {
  width: 30px;
}

footer {
  margin-top: 40px;
  color: #999;
  font-size: 0.9em;
}

/* Modo escuro */
.dark-mode {
  background-color: #1a1a1a;
  color: #f0f0f0;
}

.dark-mode h1 {
  color: #f0f0f0;
}

.dark-mode p {
  color: #ccc;
}

.dark-mode .social-links img {
  filter: invert(1);
}

.toggle-button {
  position: absolute;
  top: 10px;
  right: 10px;
  padding: 10px 15px;
  border: none;
  border-radius: 5px;
  background-color: #333;
  color: #fff;
  cursor: pointer;
  font-size: 1em;
}

.toggle-button:hover {
  background-color: #444;
}
</style>
