<template>
    <input
        :type="type"
        :style="inputStyle"
        v-model="__value"
        class="material-input-field">
</template>
<script>
export default {
    name: 'MaterialInputField',
    props: {
        value: {
            type: String,
            default: ''
        },
        type: {
            type: String,
            default: 'text'
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
    },
    data () {
        return {
            inputStyle: {
                fontSize: (this.size / 5) + 0.5 + 'em'
            }
        }
    }
}
</script>
<style>
.material-input-field {
    margin: 8px;
    border: 0.5px solid rgba(22, 22, 22, 0.1);
    box-shadow: 1px 2px 5px 0.8px rgba(22, 22, 22, 0.2);
    border-radius: 3px;
    padding: 10px;
    color: rgb(44, 44, 44);
    font-size: 1.25em;
    line-height: 1.2em;
    font-weight: 200;
    outline: none !important;
}
.material-input-field:active,
.material-input-field:focus,
.material-input-field:hover {
    outline: none !important;
}
</style>
