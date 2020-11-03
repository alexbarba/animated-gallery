<template>
  <div
    class="container self-center items-center overflow-hidden flex justify-between items-center"
  >
    <div @click="decrement">
      <ArrowLeft class="text-purple-600" />
    </div>
    <ImageView
      v-for="image in visibleImages"
      :key="image.title"
      :title="image.title"
      :description="image.description"
      :src="image.src"
    />
    <div @click="increment">
      <ArrowRight class="text-purple-600" />
    </div>
  </div>
</template>

<script>
import ArrowLeft from '../components/icons/ArrowLeft'
import ArrowRight from '../components/icons/ArrowRight'
import ImageView from '../components/ImageView'

export default {
  name: 'Carousel',
  components: {
    ArrowLeft,
    ArrowRight,
    ImageView,
  },
  props: {
    images: {
      type: Array,
      required: true,
    },
  },
  data: () => {
    return {
      pin: 0,
      visibleImages: [],
    }
  },
  mounted() {
    this.setVisibleImages()
  },

  methods: {
    increment() {
      if (this.pin < this.$props.images.length - 1) {
        this.pin++
      } else {
        this.pin = 0
      }
      this.setVisibleImages()
    },
    decrement() {
      if (this.pin > 0) {
        this.pin--
      } else {
        this.pin = this.$props.images.length - 1
      }
      this.setVisibleImages()
    },
    setVisibleImages() {
      this.visibleImages = [
        ...this.$props.images.slice(this.pin, this.pin + 3),
        ...this.$props.images.slice(
          0,
          this.pin + 3 > this.$props.images.length
            ? (this.pin + 3) % this.$props.images.length
            : 0
        ),
      ]
    },
  },
}
</script>

<style></style>
