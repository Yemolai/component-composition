<template>
    <input type="email" v-model="__value">
</template>
<script>
export default {
    name: 'InputAtom',
    props: {
        value: {
            type: String,
            default: ''
        },
        size: {
            type: Number,
            default: 1
        }
    },
    computed: {
        __value: {
            get () {
                return this.value
            },
            set (val) {
                this.$emit('input', val)
            }
        }
    }
}
</script>
<style scoped>
input {
    margin: 8px;
    border: 0.5px solid rgba(22, 22, 22, 0.1);
    box-shadow: 1px 2px 5px 0.8px rgba(22, 22, 22, 0.2);
    border-radius: 3px;
    padding: 10px;
    min-width: 10em;
    color: rgb(44, 44, 44);
    font-size: 1.25em;
    line-height: 1.2em;
    font-weight: 200;
    outline: none !important;
}
input:active,
input:focus,
input:hover {
    outline: none !important;
}
</style>

