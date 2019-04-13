<script>
import InputProton from '@/components/proton/input.vue'
export const MaterialInput = {
  name: 'InputMaterialElectron',
  components: { InputProton },
  props: {
    around: {
      default: 'div',
      type: String
    },
    bgColor: {
      default: 'white',
      type: String
    },
    textColor: {
      default: 'rgb(22, 22, 22)',
      type: String
    },
    value: {
      type: String
    }
  },
  render (h) {
    const Tag = this.around
    return (
      h(Tag, {
        class: 'material-input',
        style: {
          backgroundColor: this.bgColor,
          color: this.textColor
        },
        ...this
      }, this.$slots.default)
    )
  }
}
export default { MaterialInput }
</script>
<style>
.material-input {
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
.material-input:hover {
  outline: none !important;
}
</style>

