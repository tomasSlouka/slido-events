<template>
  <div class='container-narrow'>

    <h1>Event Creation</h1>

    <div class='grid col-2 gap-80 align-content-start'>
      <form @submit.prevent.once='addNewEvent()'>
        <div class='grid gap-20'>
          <div>
            <label for="img_url">Cover image</label>
            <input v-model='img_url' type="text" name='img_url' placeholder='Cover image'>
          </div>

          <div>
            <label for="title">Title of your event</label>
            <input v-model='title' type="text" name='title' placeholder='Title of your event'>
          </div>
          
          <div>
            <label for="short_description">Short description</label>
            <textarea v-model='short_description' type="text" name='short_description' placeholder='Write some short description of you event'></textarea>
          </div>

          <div>
            <label for="long_description">Detailed Description</label>
            <textarea v-model='long_description' type="text" name='long_description' placeholder='Write some more about your event'></textarea>
          </div>

          <div>
            <label for="price">Price</label>
            <input v-model='price' type="text" name='price' placeholder='Free or for some €?'>
          </div>
          
          <div>
            <label for="date">Date</label>
            <select v-model='date' name="date">
              <option v-for="n in 31" :key="n">{{ n }}.01.2020</option>
            </select>
          </div>
          
          <div>
            <label for="start">Start Time</label>
            <select v-model='start' name="start" placeholder='Time of start'>
              <option value='0'>0:00</option>
              <option v-for="n in 23" :key="n">{{ n }}:00</option>
            </select>
          </div>

          <div>
            <label for="end">End Time</label>
            <select v-model='end' name="end" placeholder='Time of end'>
              <option value='0'>0:00</option>
              <option v-for="n in 23" :key="n">{{ n }}:00</option>
            </select>
          </div>
          
          <button type='submit' class='button cta'>Create Event</button>
        </div>
      </form>

      <div>
        <div class='box grid gap-20 justify-items-start'>
                <img v-if='img_url != ""' :src="img_url" alt="cover">
                <img v-else src="https://via.placeholder.com/400x250/f1f1f1/dddddd?text=Cover+Image" alt="cover">
                
                <h3 v-if='title == ""'>Awesome Event</h3>
                <h3 v-else>{{ title }}</h3>

                <div class='grid col-3 auto justify-content-start gap-10'>
                    <span v-if='date == ""' class='tag gray justify-self-start'> - </span>
                    <span v-else class='tag gray justify-self-start'> {{ date }}</span>

                    <span class='tag gray justify-self-start'> {{ start }} - {{ end }}</span>
                    <span class='tag gray justify-self-end'> {{ price }} €</span>
                </div>
                <p v-if='short_description == ""' > Short description </p>
                <p v-else>{{ short_description }}</p>
                <div class='hr'></div>
                <p v-if='long_description == ""'> Detailed description </p>
                <p v-else>{{ long_description }}</p>

                <button class='mt20 button small'>Show More</button>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  data () {
        return { 
          img_url: "",
          title: "",
          short_description: "",
          long_description: "",
          price: "",
          date: "",
          start: "",
          end: "",
        }
    },

    methods: {
      async addNewEvent() {
        await this.$axios.$post('https://api.steinhq.com/v1/storages/5e2943895a823204986f3ace/Sheet1', {
          "img_url": this.img_url,
          "title": this.title,
          "short_description": this.short_description,
          "long_description": this.long_description,
          "price": this.price,
          "date": this.date,
          "start": this.start,
          "end": this.end,
        })
        .then((response) => {
            console.log(response);
            this.$router.push('/');
        }, (error) => {
            console.log(error);
            //this.res = error.response.data.message
        });
      }
    },

}
</script>

<style scoped>
.hr {
  margin-top: 20px;
  margin-bottom: 20px;
}
textarea {
  height: 150px;
}

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
