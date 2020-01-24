<template>
  <div>
    <Header />
    <EventList :eventList='eventList'/>
    <Footer />
  </div>
</template>

<script>
import Header from '~/components/Header.vue'
import EventList from '~/components/EventList.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Header, EventList, Footer
  },
  data () {
    return { 
      eventList: [
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
        {
          "id": "2",
          "title": "Collaborative Decision Making",
          "short_description": "Get your team to vote on the topics that need a democratic decision.",
          "date": "23.01.2020",
          "start": "19:00",
          "end": "20:00",
          "long_description": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam voluptate expedita eum. Ullam, reprehenderit. Libero, deserunt molestiae provident natus facere similique voluptate accusantium quis, repellendus eligendi expedita voluptates laudantium sequi. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Modi aspernatur culpa eveniet fuga soluta asperiores hic. Quam eligendi aspernatur ea officiis, tempore aliquid veritatis excepturi repellat perspiciatis ratione nulla maiores?Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid consequatur molestias provident, deleniti quia laborum asperiores repudiandae facilis voluptatum optio voluptas officia aspernatur officiis expedita incidunt eius, eligendi qui minima.",
          "img_url": "https://www.sli.do/build/img/use-case/index/slido-use-case-collaborative-decision-making-2aa35e4de4.jpg",
          "price": "15"
        },
        {
          "id": "3",
          "title": "Team Retrospective\r\n",
          "short_description": "Team retrospectives are a safe space to discuss what went well and what didn’t. Use a pre-meeting survey to collect the team’s feedback and save time for face-to-face discussion",
          "date": "24.01.2020",
          "start": "20:00",
          "end": "21:00",
          "long_description": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam voluptate expedita eum. Ullam, reprehenderit. Libero, deserunt molestiae provident natus facere similique voluptate accusantium quis, repellendus eligendi expedita voluptates laudantium sequi. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Modi aspernatur culpa eveniet fuga soluta asperiores hic. Quam eligendi aspernatur ea officiis, tempore aliquid veritatis excepturi repellat perspiciatis ratione nulla maiores?Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid consequatur molestias provident, deleniti quia laborum asperiores repudiandae facilis voluptatum optio voluptas officia aspernatur officiis expedita incidunt eius, eligendi qui minima.",
          "img_url": "https://www.sli.do/build/img/index/slido-use-case-company-meetings-6058a5eacb.jpg",
          "price": "50"
        },
        {
          "id": "4",
          "title": "Slido and Tomas Slouka joining forces?",
          "short_description": "We saw Tomas entering the headquarter of Slido at Bratislava. Tomas is know for his coding skills. He made several...",
          "date": "25.01.2020",
          "start": "21:00",
          "end": "22:00",
          "long_description": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam voluptate expedita eum. Ullam, reprehenderit. Libero, deserunt molestiae provident natus facere similique voluptate accusantium quis, repellendus eligendi expedita voluptates laudantium sequi. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Modi aspernatur culpa eveniet fuga soluta asperiores hic. Quam eligendi aspernatur ea officiis, tempore aliquid veritatis excepturi repellat perspiciatis ratione nulla maiores?Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid consequatur molestias provident, deleniti quia laborum asperiores repudiandae facilis voluptatum optio voluptas officia aspernatur officiis expedita incidunt eius, eligendi qui minima.",
          "img_url": "https://www.sli.do/build/img/index/slido-use-case-company-meetings-6058a5eacb.jpg",
          "price": "2"
        },
        {
          "id": "5",
          "title": "Don't take life so seriously.",
          "short_description": "Work-life balance, smile at people, make fun of you. Life is great, don't throw it away. LIVE IT!",
          "date": "26.01.2020",
          "start": "22:00",
          "end": "23:00",
          "long_description": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Magnam voluptate expedita eum. Ullam, reprehenderit. Libero, deserunt molestiae provident natus facere similique voluptate accusantium quis, repellendus eligendi expedita voluptates laudantium sequi. Lorem ipsum dolor sit amet, consectetur adipisicing elit. Modi aspernatur culpa eveniet fuga soluta asperiores hic. Quam eligendi aspernatur ea officiis, tempore aliquid veritatis excepturi repellat perspiciatis ratione nulla maiores?Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid consequatur molestias provident, deleniti quia laborum asperiores repudiandae facilis voluptatum optio voluptas officia aspernatur officiis expedita incidunt eius, eligendi qui minima.",
          "img_url": "https://www.sli.do/build/img/index/slido-use-case-company-meetings-6058a5eacb.jpg",
          "price": "8"
        }
      ]
     }
  },
}
</script>

<style>

</style>
