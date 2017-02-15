<template>
  <div id="app">
    <!-- Form Component goes here -->
    <Header></Header>
    <Video></Video>
  </div>
</template>

<script>
import Header from './components/Header'
import Video from './components/Video'

export default {
  name: 'app',
  data () {
  },
  mounted () {

  },
  beforeDestroy () {

  },
  components: {
    Header,
    Video
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
font-size: 24pt;

}
</style>
Contact GitHub API Training Shop Blog About
