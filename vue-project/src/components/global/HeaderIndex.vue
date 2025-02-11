<template>
  <header>
    <div class="header-container">
      <div>
        <img src="@/assets/icon/encOrangeLogo.svg" alt="Logo" />
      </div>
      <nav>
        <ul>
          <li><a>Sobre nós</a></li>
          <li><a>Features</a></li>
          <li><a>Segurança</a></li>
          <li><a>Preços</a></li>
          <li>
            <ButtonSmall
              :color="'whiter-font-color'"
              :background="'primary-color'"
              :text="'Fale conosco'"
            />
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>
<script>
import ButtonSmall from "@/components/global/ButtonSmall.vue";
export default {
  components: {
    ButtonSmall,
  },
};
</script>

<style lang="scss">
header {
  margin: 0;
  padding: 1rem 5vw; /* Usa viewport width para responsividade */
  box-sizing: border-box;
  width: 100%;
  border: 1px solid $color-border-header;
}

.header-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  height: auto;
  gap: 1rem;
}

.header-container img {
  max-width: 150px; /* Evita que a logo fique muito grande em telas pequenas */
  height: auto;
}

nav ul {
  list-style-type: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-wrap: wrap; /* Permite que itens quebrem para nova linha se necessário */
  gap: 1rem; /* Adiciona espaçamento entre os itens */
}

nav li {
  margin: 0; /* Remove margem fixa */
}

nav a {
  color: $lighter-font-color;
  text-decoration: none;
  font-size: 1rem;
  font-weight: $font-weight-medium;
}

/* Responsividade */
@media (max-width: 768px) {
  .header-container {
    flex-direction: column; /* Empilha os itens verticalmente */
    align-items: center;
  }

  nav ul {
    flex-direction: column;
    text-align: center;
  }
}
</style>
