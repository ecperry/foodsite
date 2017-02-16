<template>
  <div class="Plates">
    <p> plates</p>
    <p class = "description">
      Lorem ipsum dolor sit amet, consectetur.
    </p>
    <div id="app">
  <div class="tabs-container">
    <div class="tabs-holder" :style="{ left: computedLeftPosition }">
      <div class="tab" style="background: green">
        <img src = "../assets/merritts.png">
      </div>
      <div class="tab" style="background: red;">
        <img src = "../assets/lindas.jpg">
      </div>
      <div class="tab" style="background: blue;">
        <img src = "../assets/als.jpg">
      </div>
    </div>
  </div>

  <ul>
    <li @click="currentTab = 1">Tab 1</li>
    <li @click="currentTab = 2">Tab 2</li>
    <li @click="currentTab = 3">Tab 3</li>
  </ul>
</div>
  </div>

</template>

<script>
export default {
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
  padding-bottom: 150px;
  font-size: 24pt;

}
.description {
  font-size: 14pt;
}
body scoped {
  font-family: 'Helvetica Neue', Arial, sans-serif;
  font-size: 12px;
  color: #393939;
  text-align: center;
}
.tabs-container {
  position: relative;
  height: 400px;
  width: 600px;
  overflow: hidden;
  border: 1px solid #ccc;
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
  float: left;
}

li {
  cursor: pointer;
  font-size: 14pt;
}

li:hover {
  color: #777;
}
</style>
