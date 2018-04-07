<template lang="pug">
.comp
  nuxt-link(to='/team') RETURN_01
  .body 
    img(src='~/assets/img/Pasha.jpg')
    .content
      h2.name Павел Петров
      p.text Повелитель всей команды. Эксперт в любой сфере. Также бэкендер
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
