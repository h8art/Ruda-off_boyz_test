<template lang='pug'>
.container
  main-title(title='RUDA*OFF BOYZ')
  team
  //- Нет времени объяснять. Это костыль COMEBACK(50 раз повторяет фон с 8 картинками с разными отступами, чтоб полностью заполнить фон)
  .bg(v-for='i,index in 50')
    img(v-for='i,index in 8', :src='"/gifs/"+index+".gif"', :style='{ "top": getRandomNumTop() + "px","left": getRandomNumLeft() + "px"}')
</template>

<script>
//import названия команды в atr title передаем само название
import MainTitle from '~/components/MainTitle.vue'
//import компонента команды
import Team from '~/components/Team.vue'

export default {
  components: { MainTitle, Team },
  mounted(){
    // var gl = Object.create(glitch_exec);
    // gl.start(document.body); //активируем скрипт на глитчи
  },
  //random top и left для картинок на заднем фоне
  methods: {
    getRandomNumLeft: function(){
      return Math.random() * (1920 - 0) + 0;
    },
    getRandomNumTop: function(){
      return Math.random() * (1080 - 0) + 0;
    }
  }
}
</script>


<style lang='sass' scoped>
//scoped необходим в каждом компоненте, чтобы стили не преминялись к остальным компонентам
.container
  width: 1000px
  height: 500px
  display: flex
  align-items: center
  flex-direction: column
  background: #333
  .bg
    position: fixed
    height: 100vh
    width: 100vw
    top: -100px
    z-index: -1
    left: -100px
    img
      max-width: 250px
      max-height: 250px
      position: absolute
</style>
