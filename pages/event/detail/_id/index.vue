<template>
  <div>
    <Header />
    <EventDetail />
    <Footer />
  </div>
</template>

<script>
import Header from '~/components/Header.vue'
import EventDetail from '~/components/EventDetail.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Header, EventDetail, Footer
  },
}
</script>

<style>

</style>

