<template>
  <div class="hamburger">
    <!--
     Note: the click states and data below came from help from Seth Wright in class
     Here, I'm using a boolean to toggle the state of the panel from invisible to visible
     on click.
    -->
    <img class="button" @click="isVisible = !isVisible" src = ../../static/menu.png>
    <div class="panel" v-if="isVisible == true">
      <p class="video"><a href="#video">video</a></p>
      <p class="stories"><a href="#story">stories</a></p>
      <p class="plates"><a href="#plates">plates</a></p>
      <p class="credits"><a href="#credits">credits</a></p>

      <!--
      Anchor tag refresher from https://blog.hubspot.com/marketing/jump-link-same-page#sm.00006jfrg8p2idk6wq41exigy3tsj
      -->
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      isVisible: false
    }
  }
}
</script>

<style>
a {
color: inherit;
text-decoration: none;
}

div.panel scoped{
    padding: 0 18px;
    background-color: gray;
}

.button scoped{
  padding-right: 120px;
  cursor: pointer;
}

.credits {
  background-color: white;
  color: black;
  text-align: center;
  cursor: pointer;
}

.credits:hover {
  background-color: black;
  color: white;
  text-align: center;
  cursor: pointer;
}

.hamburger{
float: right;
background-color: white;
padding-right: 2%;
padding-top: 2%;
}

.plates {
  background-color: white;
  color: black;
  text-align: center;
  cursor: pointer;
}

.plates:hover {
  background-color: #7FBE19;
  color: white;
  text-align: center;
  cursor: pointer;
}

.stories {
  background-color: white;
  color: black;
  text-align: center;
  cursor: pointer;
}

.stories:hover {
  background-color: #98CEF0;
  color: white;
  text-align: center;
  cursor: pointer;
}

.video {
  background-color: white;
  color: black;
  text-align: center;
  cursor: pointer;
}

.video:hover {
  background-color: darkgrey;
  color: white;
  text-align: center;
  cursor: pointer;
}
</style>
