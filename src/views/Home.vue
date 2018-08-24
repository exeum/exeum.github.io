<template>
  <div>
    <Introduction />
    <Features />
    <Team />
  </div>
</template>

<script>
import Introduction from '@/components/Introduction.vue'
import Features from '@/components/Features.vue'
import Team from '@/components/Team.vue'

export default {
  name: 'home',
  components: {
    Introduction,
    Features,
    Team
  }
}
</script>
<style scoped lang="scss">
@import "../scss/res.scss";
</style>
