<template>
  <div class="Stories">
    <p> stories </p>
    <p class = "description">
      Lorem ipsum dolor sit amet, consectetur.
    </p>
    <h2>{{story.quote}}</h2>
    <p> {{story.blurb}}</p>
    <h3> {{story.name}} </h3>
  </div>
</template>

<script>
export default {
  props: [
    'story'
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
