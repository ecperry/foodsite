<template>
  <div class="Plates">
    <p class= "Title"> plates</p>
    <p class = "description">
      Lorem ipsum dolor sit amet, consectetur.
    </p>
    <div class="blob">
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

  <ul>
    <p class = "center" @click="currentTab = 1" >Merritt's BLT Sandwich</p>
    <p class = "center" @click="currentTab = 2">Linda's Cheese Fries</p>
    <p class = "center" @click="currentTab = 3">Al's Burger Shack</p>
  </ul>
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
// methods: {  }
</script>

<style>
.Plates {
  text-align: center;
  align-items: center;
}

.Title{
text-align: center;
padding-bottom: 50px;
font-size: 24pt;
}
.description {
  text-align: center;
  padding-bottom: 5px;
  font-size: 14pt;
}
img scoped{
max-width: 400px;

}
body scoped {
  font-family: 'Helvetica Neue', Arial, sans-serif;
  font-size: 12px;
  color: #393939;
  text-align: center;
}
.blob {
  width: 50%;
  max-width: 600px;
  overflow: hidden;
  cursor: pointer;
  padding-left:25%;
  
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
.center {
text-align: center;
}

.small{
  height: 100%;
  width: 100%;
}
li {
  cursor: pointer;
  font-size: 14pt;
}

li:hover {
  color: #777;
}
</style>
