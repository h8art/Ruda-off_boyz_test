<template lang="pug">
.index
  .content
    img.face.pasha(src='~/assets/img/pasha.gif')
    img.face.artem(src='~/assets/img/artem.gif')
    img.face.tazhben(src='~/assets/img/tazhben.gif')
    img.face.gosha(src='~/assets/img/gosha.gif')
    span 00:00:{{second | makeClockLike}}:{{milsecond | makeClockLike}}
</template>
<script>

export default {
  data(){
    return{
      second: 16,
      milsecond: 99
    }
  },
  mounted(){
    window.intervalID = setInterval(this.timer, 10);
  },
  filters: {
    makeClockLike: function (value) {
      if (value>=10) return value
      else return "0" + value
    }
  },
  methods: {
    //создаем таймер
    timer: function(){
      if(this.milsecond>0) this.milsecond--
      else{
        if(this.second==0&&this.milsecond==0) this.$router.push('/team');
        this.milsecond=99
        this.second--
      }
      
    }
  }
}
</script>
<style lang="sass" scoped>
.index
  background: url(/tvglitch.gif)
  width: 100vw
  height: 100vh
  background-size: 100% 110%
  background-position: -5%
  display: flex
  align-items: center
  justify-content: center
  .content
    width: 700px
    height: 300px
    background: #333
    display: flex
    align-items: center
    justify-content: center
    position: relative
    .face
      position: absolute
      width: 150px
      height: 250px
    .pasha
      left: -75px
      top: -125px
      transform: rotate(-20deg)
    .gosha
      right: -75px
      top: -125px
      transform: rotate(20deg)
    .tazhben
      left: -75px
      bottom: -125px
      transform: rotate(20deg)
    .artem
      right: -75px
      bottom: -125px
      transform: rotate(-20deg)
    span
      color: #fff
      font-size: 102px
      font-family: monospace
</style>
