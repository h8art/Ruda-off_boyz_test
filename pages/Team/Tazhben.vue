<template lang="pug">
.comp
  nuxt-link(to='/team') RETURN_01
  .body 
    img(src='~/assets/img/Tazhben.jpg')
    .content
      h2.name Никита Тажбенов
      p.text Будущий псевдо-инженер по образованию, программист(наверно) по призванию, классный парень по воле случая. В поисках Хакатона, который поможет отвлечься от факта моей собственной смертности и уйти от повседневной обыденности. Если вы уходите от самоубийства стремлением создать свой собственный смысл в жизни путем победы на Хакатоне - жмите лайк и приглашайте нашу команду на финал, ибо мы созданы друг для друга.
</template>
<style lang="sass">
.comp
  color: #fff
  max-width: 1280px
  a
    color: #fff
    text-decoration: none
    font-size: 35px
    transition: color .3s linear
    &:hover
      color: green
  .body
    display: flex
    align-items: flex-start
    img
      width: 500px
    .content
      padding-left: 30px
      font-family: 'Roboto', sans-serif
      .name
        font-size: 45px
        .text
          font-size: 25px
</style>
