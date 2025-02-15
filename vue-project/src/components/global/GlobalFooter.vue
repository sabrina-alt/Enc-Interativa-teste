<template>
  <footer>
    <div class="footer-top-section">
      <img src="@/assets/icon/encBlackLogo.svg" />
      <ul>
        <li>Sobre nós</li>
        <li>Features</li>
        <li>Segurança</li>
        <li>Preços</li>
      </ul>
      <div class="socials-section">
        <img src="@/assets/icon/InstagramIcon.svg" />
        <img src="@/assets/icon/LinkedinIcon.svg" />
      </div>
    </div>
    <div class="footer-bottom-section">
      <span class="encfy-style">
        <div>ENCFY DESIGN E TECNOLOGIA</div>
        <div>- 000.000 0001/00</div>
      </span>
      <div class="socials-section">
        <span>Política e Privacidade</span>
        <span>FAQ</span>
      </div>
    </div>
  </footer>
</template>

<script></script>

<style scoped lang="scss">
footer {
  background-color: $primary-color;
  font-family: $font-primary;
  color: $color-border-header;
  font-size: $font-size-base;
  font-weight: $font-weight-medium;
  line-height: 16px;
  max-width: 100vw;
}

.footer-top-section {
  display: flex;
  justify-content: space-around;
  align-content: center;
  align-items: center;
  height: 96px;
  border-bottom: 1px solid #c8810d;
}

ul {
  display: flex;
  flex-wrap: wrap; /* Permite quebrar os itens em várias linhas */
  justify-content: space-between; /* Espaço entre os itens */
  gap: 15px;
  list-style: none;
  max-width: 400px; /* Limita a largura para que os itens se alinhem em duas colunas */
}

.socials-section {
  display: flex;
  gap: 8px;
}

.footer-bottom-section {
  height: 85px;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.encfy-style {
  display: flex;
}

/* Media query para mobile */
@media (max-width: 768px) {
  .footer-top-section {
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: auto;
    padding: 20px 0;
  }

  .footer-top-section img {
    margin-bottom: 10px;
  }

  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 15px;
    max-width: 60%;
    padding-top: 15px;
  }

  li {
    width: 45%;
    padding-bottom: 15px;
  }

  .socials-section {
    gap: 12px;
  }

  .footer-bottom-section {
    flex-direction: column;
    align-items: center;
    height: auto;
    padding: 20px 0;
  }

  .footer-bottom-section .socials-section {
    margin-top: 10px;
    gap: 12px;
  }
  .encfy-style {
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 8px;
  }
}
</style>
