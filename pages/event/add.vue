<template>
  <div>
    <Header />
    <EventAddForm />
    <Footer />
  </div>
</template>

<script>
import Header from '~/components/Header.vue'
import EventAddForm from '~/components/EventAddForm.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Header, EventAddForm, Footer
  }
}
</script>

<style>

</style>
