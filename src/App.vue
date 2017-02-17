<template>

  <div id="app">
  <link href="https://fonts.googleapis.com/css?family=PT+Sans:700" rel="stylesheet">
  <hamburger></hamburger>
  <Top></Top>
  <Description></Description>
  <LabelS></LabelS>
  <Story v-for="story in stories" :story="story"></Story>
  <Plates></Plates>
  <Credits></Credits>
</template>

<script>
import hamburger from './components/Menu'
import Top from './components/Top'
import Description from './components/Description'
import axios from 'axios'
import Story from './components/Story'
import LabelS from './components/LabelS'
import Plates from './components/Plates'
import Credits from './components/Credits'
// attempted to make stories modals instead of a collapsible list
// import Modal from './components/Modal'
// comments below were for video attempt, used from https://www.npmjs.com/package/vue-video
// import myVideo from '../node_modules/vue-video'
// import {videoPlayer} from 'vue-video-player'

export default {
  name: 'app',
  components: {
    hamburger,
    Top,
    Description,
    Story,
    Plates,
    Credits,
    LabelS
  },
  data () {
    return {
      stories: []
    }
  },
  mounted () {
    axios.get('/static/content.json')
   .then((response) => {
     console.log(response.data)
     this.stories = response.data
   })
  }
}

// all of the comments in the section below are various failed video player attempts
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
// beforeDestroy () {
// }
// methods: {
// playerStateChanged (playerCurrentState) {
// console.log(playerCurrentState)
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
// videoPlayer,
// myVideo,
// videoPlayer,
// myVideo,
// beforeDestroy () {
// methods: {
// playerStateChanged (playerCurrentState) {
// console.log(playerCurrentState)
// },
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
</script>

<style>
body {
margin: 0px;
}

html {
font-style: normal;
font-family: 'PT Sans', sans-serif;
font-size: 14pt;
color: black;
}

h1 {
  font-style: normal;
  font-family: 'PT Sans', sans-serif;
  font-size: 28pt;
  color: black;
}
li {
  cursor: pointer;
}

li:hover {
  color: #777;
}

div {
padding-bottom: 0px;
}
.tab {
  width: 600px;
  height: 400px;
  float: left;
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
</style>
Contact GitHub API Training Shop Blog About
