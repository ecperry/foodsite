
<template>
<a id="story">
  <div class="Story">

    <!--
    Note: The event listener idea and data below started with help from Seth Wright in class
    Here, I'm toggling the class of the panel from invisible to visible with the isVisible boolean 
    -->
    <button class="accordion" @click="isVisible = !isVisible"> {{story.quote}} </button>
    <div class="panel" v-if="isVisible == true">
      <img class="square" :src="story.image">
      <p class= "blurb"> {{ story.blurb}}</p>
      <p class= "name"> - {{ story.name}}</p>
    </div>

  </div>
  </a>
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
button.accordion {
    background-color: #98CEF0;
    color: white;
    text-align: center;
    cursor: pointer;
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
    font-family: 'PT Sans', sans-serif;
    font-size: 14pt;
    font-weight: bold;
    text-align: center;
}

/* Note: the commented button classes below come from a collapsible list example on W3 Schools
/* Add a background color to the button if it is clicked on (add the .active class with JS), and when you move the mouse over it (hover) */
button.accordion.active, button.accordion:hover {
    background-color: darkgrey;
}
/* Style the accordion panel. Note: hidden by default */
div.panel {
    padding: 0 18px;
    background-color: white;
}

.blurb{
  font-style: italic;
}

.description {
  font-size: 16pt;
}

.name {
 font-weight: bold;
}

.Story{
  text-align: left;
  padding-right: 10%;
  padding-left: 10%;
}

.square {
  width: 200px;
  padding-top: 2%;
}
</style>
Contact GitHub API Training Shop Blog About
© 2017 GitHub, Inc. Terms Privacy Security Status Help
