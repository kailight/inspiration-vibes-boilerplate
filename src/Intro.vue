<template lang="pug">
#intro
  .logo-wrapper
    .logo
      .left(:class="state")
      .right(:class="state")
  .title(:class="state") Inspiration Vibes
  .subtitle(:class="state") vue2 webpack4 boilerplate
</template>

<style lang="stylus">
#intro
  display flex
  flex-direction column
  width 100%
  max-width 100%
  background-color black
  height 100vh
  overflow-x hidden

  .logo-wrapper
    height auto
    width 100%
    margin-top 3rem
    .logo
      width 36rem
      height 20rem
      display flex
      margin auto
      position relative
      .left
        background-image url("./img/leftw2.png")
        background-position right
        background-size contain
        background-repeat no-repeat
        width 100%
        height 100%
        position relative
        transition opacity 1s linear 0s, left 1s ease-out 0s
        left -18%
        opacity 0
        &.in
          opacity 1
          left 18%
      .right
        background-image url("./img/rightw2.png")
        background-position left
        background-size contain
        background-repeat no-repeat
        width 100%
        height 100%
        position relative
        right -18%
        transition opacity 1s linear 0s, right 1s ease-out 0s
        opacity 0
        right -18%
        &.in
          opacity 1
          right 18%



  .title
    text-align center
    font-family 'Raleway', sans-serif
    font-weight 300
    font-size 3rem
    margin-top 2%
    width 100%
    color #aaa
    transition opacity 2s linear 0.5s
    opacity 0
    &.in
      opacity 1

  .subtitle
    opacity 0
    text-align center
    margin-top 4%
    font-family 'Arial', sans-serif
    font-size 1rem
    color #999
    transition opacity 1.5s linear 2s
    &.in
      opacity 1

</style>

<script>
  export default {
    data() {
      return {
        state : 'out'
      }
    },
    mounted() {
      setTimeout( () => {
        this.state = 'in'
      }, 500 )
    }
  }
</script>
