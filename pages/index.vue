<template>
  <div class="container">
    <Hero />
    <LargeCardDisplay
      v-for="cardInfo in largeCardInfo"
      :key="cardInfo.id"
      :cards-section="cardInfo"
    />
    <SmallCardDisplay
      v-for="cardInfo in smallCardInfo"
      :key="cardInfo.id"
      :cards-section="cardInfo"
    />
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from '@/assets/data'
export default {
  data () {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections
    }
  }
}
</script>
