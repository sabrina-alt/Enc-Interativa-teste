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
import ButtonSmall from '@/components/global/ButtonSmall.vue'
export default {
    components: {
        ButtonSmall
    }
}
</script>

<style lang="scss">
header {
    margin: 0;  /* Garante que não há margens externas */
    padding: 0;  /* Garante que o padding não afete o layout */
    padding: 16px 80px 16px 80px;
    box-sizing: border-box;  
    width: 100%;
    border: 1px solid $color-border-header;
}
.header-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 0;
    width: 100%;
    height: 45px
}
.header-container img {
    padding: 16px 80px 16px 80px
}
nav ul {
    list-style-type: none;
    padding: 0;
    margin: 0;
    display: flex;
}
nav li {
    margin-left: 20px;
}
nav a {
    color: $lighter-font-color;
    text-decoration: none;
    font-size: $font-size-base;
    font-weight: $font-weight-medium;
    align-self: center;
    font-size: 16px;
    line-height: 20.8px;
    width: 67px;
    height: 21px;
}
</style>
