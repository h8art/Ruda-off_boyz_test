<template lang="pug">
.comp
  nuxt-link(to='/team') RETURN_01
  .body 
    img(src='~/assets/img/Gosha.jpg')
    .content
      h2.name Георгий Коняев
      p.text Любит подергать питон. На бэкенде. Шифрование, кибербезопасность и все самые крутые штуки на нем. На фото он ищет где теперь будет пить кофе после пар 
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
