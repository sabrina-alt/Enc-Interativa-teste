<template>
  <header>
    <div class="header-container">
      <div class="logo">
        <img src="@/assets/icon/encOrangeLogo.svg" alt="Logo" />
      </div>

      <button class="hamburger" @click="toggleMenu">
        <span :class="{ open: menuOpen }"></span>
        <span :class="{ open: menuOpen }"></span>
        <span :class="{ open: menuOpen }"></span>
      </button>

      <nav :class="{ open: menuOpen }">
        <ul>
          <li><a @click="closeMenu">Sobre nós</a></li>
          <li><a @click="closeMenu">Features</a></li>
          <li><a @click="closeMenu">Segurança</a></li>
          <li><a @click="closeMenu">Preços</a></li>
          <li>
            <ButtonSmall
              :color="'whiter-font-color'"
              :background="'primary-color'"
              :text="'Fale conosco'"
              @click="closeMenu"
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
  data() {
    return {
      menuOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.menuOpen = !this.menuOpen;
    },
    closeMenu() {
      this.menuOpen = false;
    },
  },
};
</script>

<style lang="scss">
header {
  margin: 0;
  padding: 1rem 5vw;
  box-sizing: border-box;
  width: 100%;
  border: 1px solid $color-border-header;
  background-color: white;
}

.header-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  height: auto;
  gap: 1rem;
}

.logo img {
  max-width: 150px;
  height: auto;
}

.hamburger {
  display: none;
  flex-direction: column;
  gap: 5px;
  background: none;
  border: none;
  cursor: pointer;
  background-color: $primary-color;
  padding: 15px;
  border-radius: 8px;
}

.hamburger span {
  width: 25px;
  height: 3px;
  background-color: $whiter-font-color;
  transition: all 0.3s;
}

.hamburger span.open:nth-child(1) {
  transform: translateY(8px) rotate(45deg);
}
.hamburger span.open:nth-child(2) {
  opacity: 0;
}
.hamburger span.open:nth-child(3) {
  transform: translateY(-8px) rotate(-45deg);
}

nav {
  display: flex;
}

nav ul {
  list-style: none;
  display: flex;
  gap: 1rem;
  padding: 0;
  margin: 0;
}

nav li {
  margin: 0;
}

nav a {
  color: $lighter-font-color;
  text-decoration: none;
  font-size: 1rem;
  font-weight: $font-weight-medium;
}

@media (max-width: 768px) {
  .hamburger {
    display: flex;
  }

  nav {
    position: absolute;
    top: 60px;
    right: 5vw;
    background: white;
    box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
    border-radius: 8px;
    padding: 1rem;
    display: none;
    flex-direction: column;
    align-items: center;
  }

  nav.open {
    display: flex;
  }

  nav ul {
    flex-direction: column;
    text-align: center;
  }
}
</style>
