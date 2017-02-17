<template>
  <div class="hamburger">
    <img class="button" @click="isVisible = !isVisible" src = ../../static/menu.png>
    <div class="panel" v-if="isVisible == true">
      <p class="menu"><a href="">VIDEO</a></p>
      <p class="menu"><a href="">STORIES</a></p>
      <p class="menu"><a href="">PLATES</a></p>
      <p class="menu"><a href="">CREDITS</a></p>
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
.hamburger{
float: right;
background-color: white;
padding-right: 2%;
padding-top: 2%;
}

.menu{
  text-align: right;
  cursor: pointer;
}

.button scoped{
  padding-right: 120px;
  cursor: pointer;
}

div.panel scoped{
    padding: 0 18px;
    background-color: gray;
  /*  display: none; */
}
</style>
