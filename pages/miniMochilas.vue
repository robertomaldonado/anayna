<template>
  <div>
    <MediaContent :item_count="6" prefix="LLV" folder="mini_mochilas"/>
  </div>
</template> 

<script>
import MediaContent from '~/components/catalog/MediaContent.vue'
export default {
  components: { MediaContent }
}
</script>
