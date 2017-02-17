
<template>
  <div class="Story">
<!--     <img class="square" :src="story.image">
  <h2>{{ story.quote }}</h2>
    <p> {{ story.blurb }}</p>
    <h3> {{ story.name }} </h3> -->
    <button class="accordion" @click="isVisible = !isVisible"> {{story.quote}} </button>
    <div class="panel" v-if="isVisible == true">
      <img class="square" :src="story.image">
      <p class= "blurb"> {{ story.blurb}}</p>
      <p class= "name">{{ story.name}}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: [
    'story'
  ],
  data () {
    return {
      isVisible: false
    }
  }
}

</script>

<style scoped>
.Story{
  text-align: left;
  padding-right: 20%;
  padding-left: 20%;
}
.description {
  font-size: 14pt;
}
.square {
  width: 200px;
}

/* Style the buttons that are used to open and close the accordion panel */
button.accordion {
    background-color: #eee;
    color: #444;
    cursor: pointer;
    padding: 3%;
    width: 100%;
    text-align: left;
    border: solid;
    border-width: thin;
    border-color: white;
    outline: none;
    transition: 0.4s;
    font-style: normal;
    font-family: sans-serif;
    font-size: 14pt;
    text-align: center;
}

/* Add a background color to the button if it is clicked on (add the .active class with JS), and when you move the mouse over it (hover) */
button.accordion.active, button.accordion:hover {
    background-color: #ddd;
}

/* Style the accordion panel. Note: hidden by default */
div.panel {
    padding: 0 18px;
    background-color: white;
  /*  display: none; */
}
</style>
Contact GitHub API Training Shop Blog About
© 2017 GitHub, Inc. Terms Privacy Security Status Help
