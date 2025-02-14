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
      <span>ENCFY DESIGN E TECNOLOGIA - 000.000 0001/00</span>
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
  justify-content: space-around;
  gap: 15px;
  list-style: none;
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
</style>
