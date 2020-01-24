<template>
  <div>
    <Header />
    <EventDetail :eventData='eventData'/>
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
    data () {
    return { 
      eventData:
        {
          "id": "1",
          "title": "Conferences",
          "short_description": "Increase audience interaction in your Q&A sessions, panel discussions or fireside chats.",
          "date": "22.01.2020",
          "start": "18:00",
          "end": "19:00",
          "long_description": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam voluptate expedita eum. Ullam, reprehenderit. Libero, deserunt molestiae provident natus facere similique voluptate accusantium quis, repellendus eligendi expedita voluptates laudantium sequi. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Modi aspernatur culpa eveniet fuga soluta asperiores hic. Quam eligendi aspernatur ea officiis, tempore aliquid veritatis excepturi repellat perspiciatis ratione nulla maiores?Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid consequatur molestias provident, deleniti quia laborum asperiores repudiandae facilis voluptatum optio voluptas officia aspernatur officiis expedita incidunt eius, eligendi qui minima.",
          "img_url": "https://www.sli.do/build/img/index/slido-use-case-company-meetings-6058a5eacb.jpg",
          "price": "5"
        },
     }
    },
}
</script>

<style>

</style>

