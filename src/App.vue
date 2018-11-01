<template>
  <div id="app">
    <opendoor-header></opendoor-header>
    <opendoor-left-navigation></opendoor-left-navigation>
    <opendoor-main-content></opendoor-main-content>
    <opendoor-contact-panel></opendoor-contact-panel>
  </div>
</template>

<script>
import OpendoorHeader from './components/Header.vue'
import OpendoorLeftNavigation from './components/LeftNavigation.vue'
import OpendoorMainContent from './components/MainContent.vue'
import OpendoorContactPanel from './components/ContactPanel.vue'

export default {
  name: 'app',
  components: {
    OpendoorHeader,
    OpendoorLeftNavigation,
    OpendoorMainContent,
    OpendoorContactPanel
  }
}
</script>

<style lang="scss">
@import './styles/variables';

html, body {
  margin: 0;
  padding: 0;
  background-color: $background;
  font-family: $font-stack;
}

a {
  color: inherit;
  text-decoration: none;
}

#app {
  display: grid;
  grid-template-columns: 1fr 230px 40px 3fr 40px 230px 1fr;
  grid-template-rows: 66px 30px 1fr;
}

</style>
