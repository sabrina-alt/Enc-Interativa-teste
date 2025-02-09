<template>
    <div>
        <a :class="buttonClasses">{{ text }}</a>
    </div>
</template>
<script>
    export default {
        props: {
            color: {
                type: Boolean,
                required: true
            },
            background: {
                type: Boolean,
                required: true
            },
            text: {
                type: String,
                required: true
            },
            icon: {
                type: String,
                default: ''
            },
            size: {
                type: Object,
                default: () => ({})
            }
            
        },
        computed: {
            buttonClasses () {
                return [
                    this.color ? `${this.color}` : '',
                    this.background ? `${this.background}` : '',
                    'size-button'
                ]
            }
        }
    }
</script>
<style lang="scss">
.size-button {
    padding: 12px 24px 12px 24px;
    border-radius: 8px;
    width: 152px;
    height: 45px;
    font-weight: $font-weight-semi-bold;
}
.whiter-font-color {
    color: $whiter-font-color;
}
.darker-font-color {
    color:$darker-font-color;
}
.text-secondary {
    color: #2ecc71;
}
.primary-color {
    background-color: $primary-color;
}
.color-border-button{
    border: 1px solid $color-border-button;
}
</style>
