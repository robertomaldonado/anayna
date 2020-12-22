<template>
  <div>
    <MediaContent :item_count="32" prefix="MLL" folder="mochilas"/>
  </div>
</template> 

<script>
import MediaContent from '~/components/catalog/MediaContent.vue'
export default {
  components: { MediaContent }
}
</script>
