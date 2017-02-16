<template>
  <div class = "Video">
    <div class= "window">
    <iframe class= "inside" src="https://www.youtube.com/embed/2V6tHv5MvFo" controls=2 color=white allowfullscreen  ></iframe>
  </div>
<p class = "Description">
  Lorem ipsum dolor sit amet, consectetur adipiscing elit,
  sed do eiusmod tempor incididunt ut labore et dolore
  magna aliqua. Ut enim ad minim veniam, quis nostrud
  exercitation ullamco laboris nisi ut aliquip ex ea commodo
  consequat.
</p>
</div>
</template>

<script>
export default {
}
// methods: {  }

// https://www.w3schools.com/html/html_youtube.asp --> this is for the iframe idea
// https://developers.google.com/youtube/player_parameters --> this is where I found YouTube parameter settings-- haven't gotten style changes to work
// https://benmarshall.me/responsive-iframes/ --> where I got the idea for the responsive css for the iframe
</script>

<style>

.Description {
padding-right: 50px;
padding-left: 50px;
padding-bottom: 10%; 
}

.window {
position: relative;
overflow: hidden;
padding-bottom: 56%;
height: 0;
border: none;

}

.inside {
width: 100%;
height: 100%;
position: absolute;
align:center;
padding-right: 0;
padding-left: 0;
padding-top: 0;
padding-bottom: 0;

}


</style>
