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
  position: relative;
  justify-content: flex-start;
  flex-direction: column;
  margin: auto;
  align-items: center;
  row-gap: 20px;
  width: 100%;
  padding-top: 50px;
  background: linear-gradient(to bottom, white 60%, $background-color-dark 40%);
  min-height: 140vh;
  font-family: $font-primary;
}
.main-container {
  font: $font-primary;
  display: flex;
  text-align: center;
  align-items: center;
  width: 886px;
  height: 296px;
  flex-direction: column;
  padding-bottom: 50px;
  gap: 16px;
  position: relative;
  top: 0px;
}
.main-container span {
  color: $primary-color;
  font-weight: $font-weight-semi-bold;
  font-size: $font-size-base;
  line-height: 20px;
  line-height: 20.8px;
}
.main-container h2 {
  font-size: $font-size-large;
  font-weight: $font-weight-regular;
  width: 886px;
  height: 146px;
  line-height: 73px;
  max-width: 100%;
}
.main-container article {
  line-height: 22px;
  font-size: $font-size-base;
  font-weight: $font-weight-regular;
  color: $lighter-font-color;
  width: 618px;
  height: 44px;
}
.button-section {
  padding-top: 10px;
  width: 340px;
  height: 45px;
  display: flex;
  gap: 16px;
}
.img-section {
  padding-top: 60px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.img-section .img {
  width: 1061px;
  height: 611px;
  border-radius: 16px;
  overflow: hidden;
}
.img-section img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: top;
}
.partner-companies {
  height: 41px;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.used-by-text {
  margin-top: 30px;
  color: $whiter-font-color;
  font-size: $font-size-base;
  font-weight: $font-weight-regular;
}
.partner-companies ul {
  list-style: none;
  padding: 10px;
  display: flex;
  align-items: center;
  justify-content: space-around;
  justify-content: center; /* Centraliza os itens */
  gap: 40px; /* Adiciona espaço entre os itens */
}
.partner-companies ul li {
  width: 160px;
  height: 41px;
  overflow: hidden;
}
.list-item {
  display: flex;
  align-items: center;
  display: flex;
  gap: 10px;
  margin-top: 10px;
}
.name-company-img,
.icon-img {
  display: flex;
  max-width: 100%;
  max-height: 100%;
  width: auto;
  height: auto;
  object-fit: contain;
  align-items: center;
}
</style>
