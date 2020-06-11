<template>
  <div class="container-fluid newsCards">
    <div class="row flex-row flex-nowrap" >
      <div class="Card-Cols col-5 align-self-center" v-for="content in content" v-bind:key="content.title">
          <div class ="card border-light" style="height:23rem">
            <img class ="card-img-top" :src="content.urlToImage">
            <div class ="card-body shadow-sm">
                <p class="card-text">{{content.title}}</p>
                <a :href="content.url" class="btn btn-primary">Visit Article</a>
            </div>
          </div>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  props: {
      content: Array
  }
}
</script>

<style scoped>
.newsCards {
  overflow-x: auto;
  white-space: wrap;
  float: none;
  padding-bottom:20px;
}

.Card-Cols{
  padding-left: 7px;
  padding-right: 7px  
}
.card-img-top {
    width: 100%;
    height: 10vw;
    object-fit: cover;
}

::-webkit-scrollbar {
  width: 10px;
}

::-webkit-scrollbar-track {
  background: #f1f1f1; 
}
 
::-webkit-scrollbar-thumb {
  background: #8BD8BD; 
}

::-webkit-scrollbar-thumb:hover {
  background: #243665; 
}
</style>