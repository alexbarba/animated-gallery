<template>
  <div class="flex align-center justify-center">
    <Carousel :images="images" />
  </div>
</template>

<script>
import Carousel from '../components/Carousel'

export default {
  name: 'AnimatedGallery',
  components: {
    Carousel,
  },
  data: () => {
    return {
      images: [
        {
          title: 'Anchorage',
          src:
            'https://upload.wikimedia.org/wikipedia/commons/thumb/4/4a/Anchorage_on_an_April_evening.jpg/1200px-Anchorage_on_an_April_evening.jpg',
          description: 'Alaska 1',
        },
        {
          title: 'Example 2',
          src:
            'https://www.cuandovisitar.es/uploads/2017/10/beste-reistijd-alaska-verenigde-staten-640x360.jpg',
          description: 'Alaska 2',
        },
        {
          title: 'Example 3',
          src:
            'https://www.fodors.com/wp-content/uploads/2019/02/HERO_Ultimate_Alaska_dreamstime_l_50550160.jpg',
          description: 'Alaska 3',
        },
        {
          title: 'Example 4',
          src:
            'https://thumbnails.expedia.com/jSRRAgOOVYDZFGAt8IKh_R7ZovA=/536x384/smart/filters:quality(60)/a.cdn-hotels.com/cos/heroimage/Anchorage_500px_66230277.jpg',
          description: 'Alaska 4',
        },
      ],
    }
  },
}
</script>
