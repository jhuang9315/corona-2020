<template>
  <div>
    <div class="jumbotron jumbotron-fluid header vertical-center" >
      <div class="col-6 header" data-aos="fade-up" data-aos-delay="500">
        <div class="container-xl site-title">
          <h1 class="display-3 Text">At home I sat...</h1>
          <p class="h4 Text">
          <br>12 weeks of isolation, 
          <br> because someone ate a bat.
          <br> Everything's closed, boredom overflowed, 
          <br> So I learned to code. 
          </p>
        </div>
      </div>
      <div class="col-6 header" data-aos="fade-up" data-aos-delay="500">
        <div class="container ">
          <img src="../assets/remote-work-man.png" width="400" height="400">
        </div>
      </div>
    </div>
      
    <div class="transition">
      <b-card class="shadow card border-light text-center" 
      data-aos="flip-left" data-aos-duration="800" id="trigger-left"
      >
        <h2 class="h2 Text">Covid Fatality Tracker</h2>
        <h6 class="card-subtitle mb-2 text-muted">Data is provide by volunteers at The Atlantic.</h6>
        <p class="card-text Text">
          <br>"The public deserves the most complete data available about COVID-19 in the US. No official source is providing it, so we are."
        </p>
      </b-card>
    </div>
  </div>
</template>

<style scoped>
.header{
  display: flex
}
.Text{
  line-height: 1.6
}
.jumbotron{
  align-items: center;
  background-color: #243665;
  color: white;
  margin-bottom: 0
}
.site-title{
  padding-left: 100px;
}
.card{
  margin: auto;
  width: 60%;
  z-index: 9;
  color: #243665;
  padding: 40px
}

.transition{
  background: linear-gradient(180deg, #243665 50%, white 50%);
}

</style>
