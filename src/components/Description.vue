<template>
  <div class = "Video">
    <div class= "window">
    <iframe class= "inside" src="https://www.youtube.com/embed/2V6tHv5MvFo" controls=2 color=white allowfullscreen  ></iframe>
  </div>
<p class = "Description">
Academia has largely dismisses the importance of food in the study of society, history, and anthropology. <span class="italic"> Food Narratives </span>strives to demonstrate the power of looking at life through
a lens of food through stories from the UNC community.
</div>
</template>

<script>
export default {
}
// methods: {  }
// NOTES:
// https://www.w3schools.com/html/html_youtube.asp --> this is for the iframe idea
// https://developers.google.com/youtube/player_parameters --> this is where I found YouTube parameter settings-- haven't gotten style changes to work
// https://benmarshall.me/responsive-iframes/ --> where I got the idea for the responsive css for the iframe
</script>

<style>

.Description {
padding-right: 10%;
padding-left: 10%;
padding-bottom: 5%;
padding-top: 4%;
color: white;
font-size: 14pt;

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

.italic {
font-style: italic;
}
.Video {
  background-color: #DA5AAA;
}

</style>
