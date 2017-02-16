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
import Description from './components/Description'
import axios from 'axios'
// import Modal from './components/Modal'
import LabelS from './components/LabelS'
import Stories from './components/Stories'
import Plates from './components/Plates'
import Credits from './components/Credits'
// below from used from https://www.npmjs.com/package/vue-video
// import myVideo from '../node_modules/vue-video'
// import {videoPlayer} from 'vue-video-player'

export default {
  name: 'app',
  data () {
    return {
      stories: [],
      currentTab: 1

    }
  },
  components: {
    hamburger,
    Top,
    Description,
    Stories,
    // Modal,
    Plates,
    Credits,
    LabelS
  },
  mounted () {
    axios.get('/static/content.json')
   .then((response) => {
     console.log(response.data)
     this.story = response.data.story
   })
  }
}

// beforeDestroy () {
// }
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
@import url('https://fonts.googleapis.com/css?family=PT+Sans');
html {
font-style: normal;
font-family: sans-serif;
font-size: 14pt;
}
body {
margin: 0px;
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
}

li:hover {
  color: #777;
}
</style>
Contact GitHub API Training Shop Blog About
