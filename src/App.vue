<template lang="pug">
#wrapper
  intro
  features
  installation
</template>

<style lang="stylus">
@import url('https://fonts.googleapis.com/css?family=Raleway:400,600&display=swap')

html
  font-size 16px

#wrapper
  display flex
  flex-direction column



</style>

<script>
import Intro from '@/Intro.vue'
import Features from '@/Features.vue'
import Installation from "@/Installation"

export default {
  components : {
    'intro' : Intro,
    'features' : Features,
    'installation' : Installation
  },
}
</script>
