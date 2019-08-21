<template lang="pug">
#installation
  .title Installation
  .blocks
    .block(:class="state")
      .items
        .item(:class="state")
          | 1.&nbsp;
          a(href="https://nodejs.org/en/download/" target="_blank") install node
        .item(:class="state")
          | 2.&nbsp;
          a(href="https://www.npmjs.com/get-npm" target="_blank") install npm
        .item(:class="state")
          | 3.&nbsp;
          a(href="https://www.atlassian.com/git/tutorials/install-git" target="_blank") install git
        .item(:class="state")
          | 4.
          | Navigate to <strong>dir</strong> using terminal/command line
        .item(:class="state")
          | 5.
          | > git clone https://github.com/kailight/inspiration-vibes-boilerplate.git
        .item(:class="state")
          | 6.
          | Navigate to <strong>dir</strong>/inspiration-vibes-boilerplate
        .item(:class="state")
          | 7.
          | > npm run dev

</template>

<style lang="stylus">
#installation
  display flex
  flex-direction column
  width 100%
  max-width 100%
  background-color #000
  height 100vh
  overflow-x hidden
  color #fff

  >.title
    font-family 'Raleway', sans-serif
    font-weight 300
    font-size 3rem
    padding 4rem 0 0 0
    width auto
    flex-grow 0
    text-align: center;

  .blocks
    flex-grow 1
    display flex
    flex-direction row

  .block
    width 100%
    padding 0 3rem 2rem 3rem
    transition opacity 2s linear 0.5s
    opacity 1
    &.in
      opacity 1

    .title
      margin auto
      font-family 'Raleway', sans-serif
      font-weight 300
      font-size 2rem
      margin-top 7%
      width auto

    .items
      text-align left
      margin-top 7%
      font-family 'Verdana', sans-serif
      font-size 0.9rem
      .item
        margin-top 2%
        a
          color #f39
          text-decoration none

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
