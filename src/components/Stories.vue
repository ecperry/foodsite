
<template>
  <div class="Stories">
    <h2>{{stories.quote}}</h2>
    <p> {{stories.blurb}}</p>
    <h3> {{stories.name}} </h3>
  </div>
</template>

<script>
export default {
  props: [
    'stories'
  ]
}
// methods: {  }
</script>

<style scoped>
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
