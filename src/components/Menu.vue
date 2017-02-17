<template>
  <div class="hamburger">
    <img class="button" @click="isVisible = !isVisible" src = ../../static/menu.png>
    <div class="panel" v-if="isVisible == true">
      <p class="video"><a href="">VIDEO</a></p>
      <p class="stories"><a href="">STORIES</a></p>
      <p class="plates"><a href="">PLATES</a></p>
      <p class="credits"><a href="">CREDITS</a></p>
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
// methods: {  }
</script>

<style>
a {
color: inherit;
text-decoration: none;
}

div.panel scoped{
    padding: 0 18px;
    background-color: gray;
  /*  display: none; */
}

.button scoped{
  padding-right: 120px;
  cursor: pointer;
}

.credits {
  background-color: #353635;
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
  background-color: #7FBE19;
  color: white;
  text-align: center;
  cursor: pointer;
}

.stories {
  background-color: #98CEF0;
  color: white;
  text-align: center;
  cursor: pointer;
}
.video {
  background-color: #DA5AAA;
  color: white;
  text-align: center;
  cursor: pointer;
}


</style>
