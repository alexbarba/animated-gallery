<template>
  <div class="flex flex-col h-screen justify-center">
    <Header />
    <Nuxt class="flex-1" />
    <Footer />
  </div>
</template>

<script>
import Header from './Header'
import Footer from './Footer'

export default {
  components: {
    Header,
    Footer,
  },
}
</script>
