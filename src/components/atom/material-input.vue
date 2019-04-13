<script>
import { MaterialInput as InputElectron } from '@/components/electron/material.vue'
export default {
  name: 'MaterialInput',
  components: { InputElectron },
  render (h) {
    const { data, props, $slots, listeners } = this
    return (
      h(InputElectron, {
        on: {...listeners},
        props: {around: 'input-proton', ...props},
        data: {...data},
      }, $slots.default)
    )
  }
}
</script>
