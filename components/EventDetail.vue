<template>
  <div class='container-narrow'>

    <h1>{{ eventData.title }}</h1>
    <div class='grid gap-80'>
      <div class='grid md-col-2 gap-80'>
        <img :src="eventData.img_url" alt="cover">
        <div class='grid gap-20 align-content-start'>
          <div class='grid col-3 auto justify-content-start gap-10'>
              <span class='tag gray justify-self-start'> {{ eventData.date }}</span>
              <span class='tag gray justify-self-start'> {{ eventData.start }} - {{ eventData.end }}</span>
              <span class='tag gray justify-self-end'> {{ eventData.price }} €</span>
          </div>
          <p class='strong'>Event Intro</p>
          <p>{{ eventData.short_description }}</p>
          <button class='button cta'>Reserve a Spot</button>
        </div>
      </div>

      <div class='grid gap-20'>
        <p class="strong">More Details About Event</p>
        <div>{{ eventData.long_description }}
      </div>

      </div>
    </div>

    <h3></h3>
  </div>
</template>

<script>
export default {
    props: ['eventData'],

    data () {
        return { 

        }
    },
}
</script>

<style scoped>

</style>
