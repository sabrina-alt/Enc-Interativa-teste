<template>
  <section>
    <div class="section-title">
      <span class="orange-text">PLANOS & PREÇOS</span>
      <h2>Planos & Preços</h2>
    </div>
    <div class="cards-style">
      <div class="individual-card-first">
        <div>
          <TitleCard :title="'Basic'" :price="'R$ 15.000,00'" />
          <SeparatorLine />
          <div>
            <CardContentList />
          </div>
          <div class="btn-section">
            <SeparatorLine />
            <ButtonSmall
              :text="'Escolher este plano'"
              :background="'color-button-grey'"
              :color="'whiter-font-color'"
              :size="'medium-size'"
            />
          </div>
        </div>
      </div>
      <div class="individual-card-center">
        <div>
          <TitleCard :title="'Standard'" :price="'R$ 18.000,00'" />
          <SeparatorLine />
          <div>
            <CardContentList :background-color="'primary-color'" />
          </div>
          <div class="btn-section">
            <SeparatorLine />
            <ButtonSmall
              :text="'Escolher este plano'"
              :background="'primary-color'"
              :color="'whiter-font-color'"
              :size="'medium-size'"
            />
          </div>
        </div>
      </div>
      <div class="individual-card-last">
        <div>
          <TitleCard :title="'Premium'" :price="'R$ 20.000,00'" />
          <SeparatorLine />
          <div>
            <CardContentList />
          </div>
          <div class="btn-section">
            <SeparatorLine />
            <ButtonSmall
              :text="'Escolher este plano'"
              :background="'color-button-grey'"
              :color="'whiter-font-color'"
              :size="'medium-size'"
            />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import CardContentList from "@/components/plansAndPricesSection/CardContentList.vue";
import TitleCard from "@/components/plansAndPricesSection/TitleCard.vue";
import SeparatorLine from "@/components/global/SeparatorLine.vue";
import ButtonSmall from "@/components/global/ButtonSmall.vue";

export default {
  components: {
    CardContentList,
    TitleCard,
    SeparatorLine,
    ButtonSmall,
  },
};
</script>

<style scoped lang="scss">
@import "@/assets/scss/utils.scss";

section {
  padding: 50px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  background-color: $background-color-light;
}

.section-title {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.btn-section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-content: center;
  align-items: center;
}

.orange-text {
  @extend .orange-text;
}

h2 {
  @extend .main-title;
  color: $whiter-font-color;
}

.cards-style {
  display: flex;
  justify-content: space-between;
  gap: 0;
  align-items: center;
}

.individual-card-last,
.individual-card-first,
.individual-card-center {
  @extend .card-plans;
  width: 321px;
  height: 522px;
  border-radius: 16px;
}

.individual-card-center {
  height: 570px;
  padding-top: 10px;
}

.individual-card-first {
  border-radius: 16px 0 0 16px;
}

.individual-card-last {
  border-radius: 0 16px 16px 0;
}

.individual-card-center .btn-section {
  margin-top: 30px;
}

@media (max-width: 768px) {
  .cards-style {
    flex-direction: column;
    align-items: flex-start;
    gap: 20px;
  }

  .individual-card-first,
  .individual-card-center,
  .individual-card-last {
    width: 100%;
    height: auto;
    border-radius: 16px;
  }

  .section-title h2 {
    text-align: center;
    line-height: 57px;
    padding-bottom: 30px;
    width: 100%;
  }
  .individual-card-last,
  .individual-card-first,
  .individual-card-center {
    padding-bottom: 25px;
  }
}
</style>
