<template>
  <div class='container-narrow grid gap-20'>

      <h1>Find events near to you</h1>
      <div class='wrapper grid col-1 md-col-2 lg-col-2 gap-80 align-items-start'>
          <div v-for="item in eventList" :key="item.id" class='box grid gap-20 justify-items-start'>
                <img :src="item.img_url" alt="cover">
                <h3>{{ item.title }}</h3>
                <div class='grid col-3 auto justify-content-start gap-10'>
                    <span class='tag gray justify-self-start'> {{ item.date }}</span>
                    <span class='tag gray justify-self-start'> {{ item.start }} - {{ item.end }}</span>
                    <span class='tag gray justify-self-end'> {{ item.price }} €</span>
                </div>
                <p>{{ item.short_description }}</p>
                <nuxt-link :to='"/event/detail/" + item.id' tag='button' class='button small'>Show More</nuxt-link>
          </div>
      </div>

  </div>
</template>

<script>
export default {
    props: ['eventList'],

    data () {
        return { 

        }
    },
}
</script>

<style scoped>
.box {
  position: relative;
  border-radius: 5px;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  padding: 20px;
  -webkit-transition: all 0.6s cubic-bezier(0.165, 0.84, 0.44, 1);
  transition: all 0.6s cubic-bezier(0.165, 0.84, 0.44, 1);
}

.box::after {
  content: "";
  border-radius: 4px;
  position: absolute;
  z-index: -1;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
  opacity: 0;
  -webkit-transition: all 0.6s cubic-bezier(0.165, 0.84, 0.44, 1);
  transition: all 0.6s cubic-bezier(0.165, 0.84, 0.44, 1);
}

.box:hover {
  -webkit-transform: scale(1.05, 1.05);
  transform: scale(1.05, 1.05);
}

.box:hover::after {
    opacity: 1;
}
.box h3 {
    font-size: 20px;
}
</style>
