<template>
  <div id="app">
    <!-- Form Component goes here -->
    <Header></Header>
    <div class = "container">
        <my-video :sources="video.sources" :options="video.options"></my-video>
    <Video :options="videoOptions"></Video>
  </div>
  <Description></Description>
  <Stories></Stories>
</template>

<script>
import Header from './components/Header'
import myVideo from '../node_modules/vue-video'
import Description from './components/Description'
import Stories from './components/Stories'

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
      }
    }
  },
  mounted () {

  },
  beforeDestroy () {

  },
  components: {
    Header,
    myVideo,
    Description,
    Stories
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
