<template>
  <div>
    <div class="Coronanews">
      <div class="Transition"></div>
      <div class="container News" data-aos="fade-right" data-aos-duration="1000">
        <div class="row">      
          <div class= "col-6 col-md-4 align-self-center">
            <h1>Some Positivity </h1>
            <p1>Here is some good news to chear you up. Articles provided by the newsapi from various publications.</p1>
          </div>

          <div class= "col-12 col-md-8">     
            <Content v-bind:content="arrArticles"></Content>
          </div>

        </div>
      </div>
    </div>
  </div>    
</template>

<script>
import axios from 'axios' 
import Content from './Content.vue'
export default {
  components: {
      Content
  },
  data() {
    return {
      apiKey:'eaf38a5126094199acbeae0ea0a5f1db',
      arrArticles: [],
    }
  },
  created () {
    axios.get('https://newsapi.org/v2/everything?q=happy-uplifting-smile&apiKey='+this.apiKey)
      .then(response => {
        this.arrArticles = response.data.articles

    })
  },
}
</script>

<style scoped>
.News{
  padding-bottom:30px;
  color: #243665
}

.Coronanews{
background: #F0F8FF
}

.Transition{
  height: 180px;
  background: linear-gradient(184deg,white 50%,#F0F8FF 50%);
  width: 100%;
}

</style>