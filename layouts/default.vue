<template lang='pug'>
.main-layout(v-if='start')
  audio(autoplay)
    source(src="/hackersmusic.mp3" type="audio/mp3")
  //- transition - анимация для router-view(nuxt)
  transition(name='fade' mode="out-in")
    nuxt
</template>
<script>
export default {
  data(){
    return{
      start: false
    }
  },
  mounted(){
    this.start=confirm("Нажимая ок, вы подверждаете, что не страдаете эпилепсией. Мы предупредили. Также на странице музыка и различные звуки. Рекомендуем надеть наушники")
  }
}
</script>

<style lang='sass'>
body
  background: #333
  margin: 0
  font-family: "Exo", sans-serif
  overflow: hidden //Скрываем глитчи из-за которых появляется скролл
  height: 100vh //задаем телу высоту в размер монитора
  display: flex
  align-items: center
  justify-content: center //Выравниваем контейнер внутри по центру
//анимация входа и выхода страницы
.fade-enter-active, .fade-leave-active 
  transition: opacity .5s
.fade-enter, .fade-leave-to 
  opacity: 0
</style>
