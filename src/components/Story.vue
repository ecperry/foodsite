
<template>
  <div class="Story">
    <h2>{{story.quote}}</h2>
    <p> {{story.blurb}}</p>
    <h3> {{story.name}} </h3>
  </div>
</template>

<script>
export default {
  props: [
    'stories'
  ],
}
</script>

<style scoped>
.Story{
}
.Stories {
  text-align: center;
  padding-bottom: 150px;
  font-size: 24pt;
}
.description {
  font-size: 14pt;
}
</style>
Contact GitHub API Training Shop Blog About
© 2017 GitHub, Inc. Terms Privacy Security Status Help
