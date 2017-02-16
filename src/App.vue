<template>
  <div id="app">
    <!-- Form Component goes here -->
    <hamburger></hamburger>
  <Top></Top>
  <Description></Description>
  <LabelS></LabelS>
  <Stories v-for="story in stories" :story="story"></Stories>
  <Plates ></Plates>

  <Credits></Credits>
</template>

<script>
import hamburger from './components/Menu'
import Top from './components/Top'
// below from used from https://www.npmjs.com/package/vue-video
// import myVideo from '../node_modules/vue-video'
  // import {videoPlayer} from 'vue-video-player'
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
// all of the below are various video player attempts
// video: {
// sources: [{
// src: 'assets/FoodStories.mp4',
// type: 'video/mp4'
// }],
// options: {
// autoplay: true,
// volume: 0.6,
// poster: ''
// }
// },
// would need this in HTML above:
// <div class = "container">
// <my-video :sources="video.sources" :options="video.options"></my-video>
// <Video :options="videoOptions"></Video>
// new
// videoOptions: {
// source: {
// type: 'video/youtube',
// src: 'https://www.youtube.com/watch?v=2V6tHv5MvFo&t=1s'
// },
// techOrder: ['youtube'],
// autoplay: false,
// controls: false,
// ytControls: true
// would need this for HTML
// <video-player :options="videoOptions" @player-state-changed="playerStateChanged"></video-player>
//   },
      stories: [

      ]
    }
  },

  components: {
    hamburger,
    Top,
// videoPlayer,
// myVideo,
    Description,
    Stories,
    Plates,
    Credits,
    LabelS
  },
// methods: {
// playerStateChanged (playerCurrentState) {
// console.log(playerCurrentState)
// },
  mounted () {
    axios.get('/static/content.json')
    .then((response) => {
      console.log(response.data)
      this.story = response.data.story
    })
  }
// beforeDestroy () {
// }
}

</script>

<style>
@import url('https://fonts.googleapis.com/css?family=PT+Sans');
html {
font-style: normal;
font-family: sans-serif;
font-size: 14pt;
}
body {
margin: 0px;
}
</style>
Contact GitHub API Training Shop Blog About
