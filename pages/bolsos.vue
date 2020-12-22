<template>
  <div>
    <MediaContent :item_count="7" prefix="BOL" folder="bolsos"/>
  </div>
</template> 

<script>
import MediaContent from '~/components/catalog/MediaContent.vue'
export default {
  components: { MediaContent }
}
</script>
