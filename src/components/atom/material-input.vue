<script>
import { MaterialInput as InputElectron } from '@/components/electron/material.vue'
export default {
  name: 'MaterialInput',
  components: { InputElectron },
  render (h) {
    const { data, props, $slots, listeners } = this

    const attrbs = {
      on: {...listeners},
      props: {around: 'input-proton', ...props},
      data: {...data},
    }

    return (
      h(InputElectron, attrbs, $slots.default)
    )
  }
}
</script>
