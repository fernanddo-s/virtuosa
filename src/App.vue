<template>

  <div class="landing-page">
    <header>
      <!-- Logo da Loja -->
      <img src="@/assets/logo-vt.png" alt="Logo da Loja" class="logo" />
    </header>

    <section class="info-section">
      <h1>{{ lojaNome }}</h1>
      <p class="description">{{ descricaoLoja }}</p>
      <p>🌻 Especialista em T-shirts</p>
      <p>📍Lagoa do Carneiro - Acaraú</p> 
      <p>✨ Trabalhamos com Cosméticos</p>
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

<script>
export default {
  data() {
    return {
      lojaNome: 'Virtuosa',
      descricaoLoja:
        'Bem-vindos à Virtuosa! Oferecemos produtos de alta qualidade diretamente para você. ',
      contatoLoja: 'Entre em contato:',
      socialLinks: {
        instagram: 'https://www.instagram.com/virtuosa_bf/',
        whatsapp: 'https://wa.me/558899516865',
      }
    }
  }
}
</script>

<style scoped>
/* Estilo para centralizar a página e dar uma boa apresentação */
.landing-page {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  height: 100vh;
  background-color: #f4f4f4;
  font-family: 'Arial', sans-serif;
}

.description{
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
</style>
