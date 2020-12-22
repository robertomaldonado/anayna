<template>
  <div>
    <MediaContent :item_count="50" prefix="LAZ" folder="lazos"/>
  </div>
</template> 

<script>
import MediaContent from '~/components/catalog/MediaContent.vue'
export default {
  components: { MediaContent }
}
</script>
