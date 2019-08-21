<template lang="pug">
#features
  .title Features
  .blocks
    .packages.block(:class="state")
      .title Packages
      .items
        .item(:class="state") vue2
        .item(:class="state") webpack4
        .item(:class="state") pug
        .item(:class="state") stylus
        .item(:class="state")
          | @babel/core
          | with
          | core-js

    .components.block(:class="state")
      .title Components
      .items
        .item 3 simple block components:
        .item Intro
        .item Features
        .item Installation

</template>

<style lang="stylus">
#features
  display flex
  flex-direction column
  width 100%
  max-width 100%
  background-color #eee
  height 100vh
  overflow-x hidden
  color #222

  >.title
    font-family 'Raleway', sans-serif
    text-align center
    font-weight 300
    font-size 3rem
    padding 4rem 0 0 0
    width auto
    flex-grow 0

  .blocks
    display flex
    flex-direction row
    flex-grow 1

  .block
    width 50%
    padding 3rem

  .packages, .components
    transition opacity 1s linear 0.5s
    opacity 0
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
      font-family 'Arial', sans-serif
      font-size 1rem
      .item
        margin-top 2%

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
