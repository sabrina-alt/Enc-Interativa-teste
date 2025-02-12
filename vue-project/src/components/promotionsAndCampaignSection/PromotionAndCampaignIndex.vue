<template>
  <section>
    <div class="main-container">
      <span> O QUE É O ENCFY </span>
      <h2>Plataforma para o suporte de promoções e campanhas</h2>
      <article>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur hendrerit orci
        at tellus consequat hendrerit. Pellentesque porta ullamcorper nisl,
      </article>
      <div class="button-section">
        <div>
          <ButtonSmall
            :color="'whiter-font-color'"
            :background="'primary-color'"
            :text="'Fale conosco'"
          />
        </div>
        <div>
          <ButtonSmall
            :color="'darker-font-color'"
            :background="'color-border-button'"
            :text="'Planos e Preços'"
          />
        </div>
      </div>
    </div>
    <div class="img-section">
      <img class="img" src="@/assets/img/landingPageImg.png" />
    </div>
    <div class="partner-companies">
      <div class="used-by-text">Usado por grandes empresas do Brasil:</div>
      <ul>
        <li class="list-item" v-for="(item, index) in companyList" :key="index">
          <div>
            <img class="icon-img" :src="item.iconPath" />
          </div>
          <img class="name-company-img" :src="item.companyNamePath" />
        </li>
      </ul>
    </div>
  </section>
</template>
<script>
import ButtonSmall from "@/components/global/ButtonSmall.vue";
export default {
  components: {
    ButtonSmall,
  },
  data() {
    return {
      companyList: [
        {
          iconPath: "public/img/glossyIcon.svg",
          companyNamePath: "public/img/glossy.svg",
        },
        {
          iconPath: "public/img/umbrellaIcon.svg",
          companyNamePath: "public/img/umbrella.svg",
        },
        {
          iconPath: "public/img/rechargeIcon.svg",
          companyNamePath: "public/img/recharge.svg",
        },
        {
          iconPath: "public/img/pinPointIcon.svg",
          companyNamePath: "public/img/pinPoint.svg",
        },
        {
          iconPath: "public/img/cactusIcon.svg",
          companyNamePath: "public/img/cactus.svg",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
section {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  padding: 5vh 5vw;
  background: linear-gradient(to bottom, white 60%, $background-color-dark 40%);
  min-height: auto;
  font-family: $font-primary;
}
span {
  color: $primary-color;
  font-size: $font-size-base;
  font-weight: $font-weight-semi-bold;
}
.main-container {
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 100%;
  padding-bottom: 50px;
  gap: 1rem;
}

.main-container h2 {
  color: $darker-font-color;
  font-size: $font-size-large;
  font-weight: $font-weight-regular;
  width: 886px;
  text-align: center;
  line-height: 1.2;
}

.main-container article {
  font-size: $font-size-base;
  color: $lighter-font-color;
  font-weight: $font-weight-regular;
  width: 618px;
  height: 44px;
}

.button-section {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1rem;
  padding-top: 10px;
}

.img-section {
  padding-top: 60px;
  display: flex;
  justify-content: center;
  align-items: center;
  max-width: 100%;
}

.img-section .img {
  width: 1061px;
  height: 611px;
  border-radius: 16px;
  overflow: hidden;
  object-fit: cover;
  object-position: top;
}

.partner-companies {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  padding: 2rem 0;
  width: 100%;
}

.partner-companies ul {
  padding: 0;
  list-style: none;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 3rem;
}

.partner-companies ul li {
  width: auto;
  max-width: 160px;
}

.list-item {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}
.used-by-text {
  color: $whiter-font-color;
  font-size: $font-size-base;
  font-weight: $font-weight-regular;
  margin-bottom: 1rem;
}
@media (max-width: 768px) {
  .main-container {
    max-width: 95%;
  }
  .main-container article {
    max-width: 100%;
  }
  .main-container h2 {
    max-width: 100%;
  }
  .button-section {
    flex-direction: column;
    align-items: center;
  }
  .partner-companies ul {
    gap: 1rem;
  }
}
</style>
