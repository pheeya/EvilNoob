<template>
  <div id="app">
  <head><meta name="viewport" content="width=device-width, initial-scale=1"></head>
<cmp-nav></cmp-nav>
<cmp-slide></cmp-slide>
<cmp-Icons></cmp-Icons>
<cmp-line></cmp-line>
<cmp-Stories imgLink1= "https://bnetcmsus-a.akamaihd.net/cms/blog_thumbnail/6G35EETFRBVG1559175082219.jpg"></cmp-Stories>
<cmp-Worlds></cmp-Worlds>
 <cmp-footer></cmp-footer>
  </div>
</template>

<script>
import worlds from "./components/creatWorlds"
import nav from "./components/nav"
import slides from "./components/slide"
import gameIcons from "./components/gameIcons"
import singleLine from "./components/singleLine"
import topStories from "./components/topStories"
import footer from "./components/footer"
export default {
components: 
{
  cmpNav: nav,
  cmpSlide:slides,
  cmpIcons:gameIcons,
  cmpLine:singleLine,
  cmpStories:topStories,
  cmpWorlds:worlds,
  cmpFooter:footer
}
}
</script>

<style scoped>
#app
{
  
height:100vh;
}

</style>
