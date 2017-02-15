<template>
  <div id="app">
    <!-- Form Component goes here -->
    <Menu></Menu>
    <Top></Top>
    <div class = "container">
        <my-video :sources="video.sources" :options="video.options"></my-video>
    <Video :options="videoOptions"></Video>
  </div>
  <Description></Description>
  <Stories v-for="story in stories" :story="stories"></Stories>
  <Plates></Plates>
  <Credits></Credits>
</template>

<script>
import Menu from './components/Menu'
import Top from './components/Top'
import myVideo from '../node_modules/vue-video'
import Description from './components/Description'
import axios from 'axios'
import Stories from './components/Stories'
import Plates from './components/Plates'
import Credits from './components/Credits'

export default {
  name: 'app',
  // below from used from https://www.npmjs.com/package/vue-video
  // so far, not working...
  data () {
    return {
      video: {
        sources: [{
          src: 'assets/FoodStories.mp4',
          type: 'video/mp4'
        }],
        options: {
          autoplay: true,
          volume: 0.6,
          poster: ''
        }
      },
      stories: []
    }
  },
  mounted () {
    axios.get('/static/content.json')
    .then((response) => {
      console.log(response.data)
      this.stories = response.data
    })
  },
  beforeDestroy () {

  },
  components: {
    Menu,
    Top,
    myVideo,
    Description,
    Stories,
    Plates,
    Credits
  },
  methods: {
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
