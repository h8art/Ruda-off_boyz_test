<template lang="pug">
  h1(class="glitch",:data-text="title") {{title}}
</template>
<script>
export default {
  //указываем, что нам прийдет проп через атрибут title
  props: ['title']
}
</script>

<style lang="scss" scoped>
// Заимствуем стили с https://codepen.io/hi-im-si/pen/oXyqjG?q=text%20glitch&order=popularity&depth=everything&show_forks=false
$primaryColor: #fff;
$secondaryColor: #333;
$steps: 20;


.glitch {
  position: relative;
  margin: 0 auto;
  color: $primaryColor;
  font-size: 80px;
  font-family: "Exo", sans-serif;
  font-weight: 600;
  text-align: center;
  text-transform: uppercase;
  letter-spacing: 0.01em;
  transform: scale3d(1,1,1);
  

  &::before,
  &::after {
    content: attr(data-text);
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    overflow: hidden;
    background: $secondaryColor;
    color: $primaryColor;
    clip: rect(0, 900px, 0, 0);

  }

  &::before {
    left: 7px;
    text-shadow: 1px 0 green;
    animation: glitch-effect 3s infinite linear alternate-reverse;
  }

  &::after {
    left: 3px;
    text-shadow: -1px 0 red;
    animation: glitch-effect 2s infinite linear alternate-reverse;
  }
}

@keyframes glitch-effect{
  @for $i from 0 through $steps{
    #{percentage($i*(1/$steps))}{
      clip:rect(random(100)+px,9999px,random(100)+px,0);
    }
  }
    
}
</style>
