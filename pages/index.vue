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
          "long_description": "TestTest",
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
          "long_description": "TestTest",
          "img_url": "https://www.sli.do/build/img/use-case/index/slido-use-case-collaborative-decision-making-2aa35e4de4.jpg",
          "price": "5"
        },
        {
          "id": "3",
          "title": "Team Retrospective\r\n",
          "short_description": "Team retrospectives are a safe space to discuss what went well and what didn’t. Use a pre-meeting survey to collect the team’s feedback and save time for face-to-face discussion",
          "date": "24.01.2020",
          "start": "20:00",
          "end": "21:00",
          "long_description": "TestTest",
          "img_url": "https://www.sli.do/build/img/index/slido-use-case-company-meetings-6058a5eacb.jpg",
          "price": "5"
        },
        {
          "id": "4",
          "title": "Test",
          "short_description": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quia aperiam pariatur perferendis fugiat culpa deleniti rerum maiores distinctio, dicta ipsam.\n",
          "date": "25.01.2020",
          "start": "21:00",
          "end": "22:00",
          "long_description": "TestTest",
          "img_url": "https://www.sli.do/build/img/index/slido-use-case-company-meetings-6058a5eacb.jpg",
          "price": "5"
        },
        {
          "id": "5",
          "title": "Test",
          "short_description": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quia aperiam pariatur perferendis fugiat culpa deleniti rerum maiores distinctio, dicta ipsam.\n",
          "date": "26.01.2020",
          "start": "22:00",
          "end": "23:00",
          "long_description": "TestTest",
          "img_url": "https://www.sli.do/build/img/index/slido-use-case-company-meetings-6058a5eacb.jpg",
          "price": "5"
        }
      ]
     }
  },
  // async asyncData({ $axios }) {
  //     const eventList = await $axios.$get('https://api.steinhq.com/v1/storages/5e2943895a823204986f3ace/Sheet1')
  //     return { eventList }
  // }

  // 734693915972-nq81krj2ouimfm3mkoamu7nsq139alqv.apps.googleusercontent.com - client id
  // ZqV5ejmIIVi3Z-Y1-u4y2NwH - client secret
  // AIzaSyBjSLKEKBSctGmn6cMH7jFauGr4D80N7-o - api key
}
</script>

<style>

</style>
