<template>
  <div>
    <MediaContent :item_count="4" prefix="CCJ" folder="carteras_conejo"/>
  </div>
</template> 

<script>
import MediaContent from '~/components/catalog/MediaContent.vue'
export default {
  components: { MediaContent }
}
</script>
