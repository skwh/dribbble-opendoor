<template>
  <nav>
    <div id="main-links">
      <nav-button v-for="(navItem, index) in navItems"
                  :key="`navButton-${index}`"
                  :selected="index==0"
                  :icon="navItem.icon">
                  {{ navItem.text }}
                </nav-button>
    </div>
    <hr />
    <div id="secondary-links">
      <nav-button>Help?</nav-button>
      <nav-button icon="open_in_new" reversed="true">Opendoor.com</nav-button>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'OpendoorLeftNavigation',
  data () {
    return {
      navItems: [
        {
          text: 'Summary',
          icon: 'notes'
        },
        {
          text: 'Contract',
          icon: 'description'
        },
        {
          text: 'Assessment',
          icon: 'home'
        },
        {
          text: 'Closing',
          icon: 'check'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import '../styles/variables';

nav {
  grid-column-start: 2;
  grid-row-start: 3;

  hr {
    border: none;
    border-top: 1px solid $light-grey;
  }

  #secondary-links {
    * {
      position: relative;
      left: 1vw;
    }
  }
}
</style>
