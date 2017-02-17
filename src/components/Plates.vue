<template>
  <div class="Plates">
    <p class= "Title"> plates</p>
    <p class = "description">
      Click a restaurant in the list below to get a glimpse of a bacon-filled
      Chapel Hill favorite.
      </p>
  </p>
    <div class="blob">
    <ul>
      <p class = "center" @click="currentTab = 1" >Merritt's BLT Sandwich</p>
      <p class = "center" @click="currentTab = 2">Linda's Cheese Fries</p>
      <p class = "center" @click="currentTab = 3">Al's Burger Shack</p>
  </ul>
  <div class="tabs-container">
    <div class="tabs-holder" :style="{ left: computedLeftPosition }">
      <div class="tab">
        <img src = "../../static/merritts.png" class="small">
      </div>
      <div class="tab">
        <img src = "../../static/lindas.jpg"class="small">
      </div>
      <div class="tab">
        <img src = "../../static/als.jpg" class="small">
      </div>
    </div>
  </div>

<p class = "block">
  Bacon has long been a staple of the Southern American cuisine. Dating
  back to early settlers, pork was relied upon as a valuable source of protein.
  Bacon grease was a prominent cooking ingredient in the
  slave-operated plantation kitchens that characterized Southern food throughout
  the Civil War.
</p>
</div>
</div>

</template>

<script>
export default {
  props: [
    'plate'
  ],
  data () {
    return {
      currentTab: 1
    }
  },
  computed: {
    computedLeftPosition () {
      return ((this.currentTab - 1) * -600) + 'px'
    }
  }
}
</script>

<style>

body scoped {
  font-family: 'Helvetica Neue', Arial, sans-serif;
  font-size: 12px;
  color: #393939;
  text-align: center;
}

img scoped{
max-width: 400px;
}

li {
  cursor: pointer;
  font-size: 14pt;
}

li:hover {
  color: #777;
}

.blob {
  width: 50%;
  max-width: 600px;
  overflow: hidden;
  cursor: pointer;
  padding-left:25%;
  padding-bottom: 10%;
}

.block{
  text-align: center;

}

.center {
text-align: center;
}

.description {
  text-align: center;
  padding-bottom: 5px;
  font-size: 14pt;
  padding-right: 25%;
  padding-left: 25%;
}

.Plates {
  text-align: center;
  align-items: center;
}

.small{
  height: 100%;
  width: 100%;
}

.Title{
text-align: center;
padding-bottom: 5px;
padding-top: 10%;
font-size: 30pt;
}

.tabs-container {
  position: relative;
  height: 400px;
  width: 600px;
  overflow: hidden;
  border: 1px solid #black;
}

.tabs-holder {
  position: absolute;
  width: 1800px;
  top: 0;
  left: 0;
  transition: left 0.75s;
}

.tab {
  width: 600px;
  height: 400px;
}

</style>
