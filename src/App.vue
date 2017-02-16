<template>
  <div id="app">
    <!-- Form Component goes here -->
    <hamburger></hamburger>
  <Top></Top>
  <Description></Description>
  <LabelS></LabelS>
  <Stories v-for="story in stories" :story="story"></Stories>
  <Plates></Plates>
  <Credits></Credits>
</template>

<script>
import hamburger from './components/Menu'
import Top from './components/Top'
// below from used from https://www.npmjs.com/package/vue-video
// import myVideo from '../node_modules/vue-video'
import Description from './components/Description'
import axios from 'axios'
import LabelS from './components/LabelS'
import Stories from './components/Stories'
import Plates from './components/Plates'
import Credits from './components/Credits'
export default {
  name: 'app',

  data () {
    return {
    //  video: {
    //    sources: [{
    //      src: 'assets/FoodStories.mp4',
    //      type: 'video/mp4'
      //  }],
    //    options: {
      //    autoplay: true,
  //        volume: 0.6,
    //      poster: ''
    //    }
    //  },

  // would need this in HTML above:
// <div class = "container">
// <my-video :sources="video.sources" :options="video.options"></my-video>
// <Video :options="videoOptions"></Video>
      stories: [

      ]
    }
  },
  components: {
    hamburger,
    Top,
//    myVideo,
    Description,
    Stories,
    Plates,
    Credits,
    LabelS
  },
  methods: {
  },
  mounted () {
    axios.get('/static/content.json')
    .then((response) => {
      console.log(response.data)
      this.story = response.data.story
    })
  },
  beforeDestroy () {
  }

}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=PT+Sans');
html {
font-style: normal;
font-family: sans-serif;
font-size: 14pt;
}
</style>
Contact GitHub API Training Shop Blog About
