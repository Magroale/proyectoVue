<template>
  <div id="app">
    <Navbar/>
    <SectionOne/>
    <SectionTwo/>
    <SectionThree/>
    <SectionFour/>
    <SectionFive/>
    <SectionSix/>
    <SectionFinal/>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import SectionOne from './components/SectionOne.vue'
import SectionTwo from './components/SectionTwo.vue'
import SectionThree from './components/SectionThree.vue'
import SectionFour from './components/SectionFour.vue'
import SectionFive from './components/SectionFive.vue'
import SectionSix from './components/SectionSix.vue'
import SectionFinal from './components/SectionFinal.vue'


export default {
  name: 'App',
  components: {
    Navbar,
    SectionOne,
    SectionTwo,
    SectionThree,
    SectionFour,
    SectionFive,
    SectionSix,
    SectionFinal,
  }
}
</script>

<style>

</style>
