<script>
export default {
    name: 'VText',
    props: {
        el: {
            type: String,
            default: 'span'
        }
    },
    render (h) {
        return (
            h(this.el, {}, this.$slots.default)
        )
    }
}
</script>

