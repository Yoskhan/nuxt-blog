<template>
  <div>
    <TheHeader @sidenavtoggle="displaySidenav = true" />
    <TheSidenav :show="displaySidenav" @close="displaySidenav = false" />
    <TheSideNavToggle />
    <Nuxt />
  </div>
</template>

<script>
import TheHeader from '~/components/Navigation/TheHeader' 
import TheSidenav from '~/components/Navigation/TheSidenav' 
import TheSideNavToggle from '~/components/Navigation/TheSideNavToggle'

export default {
  components: {
    TheHeader,
    TheSidenav,
  },
  data() {
    return {
      displaySidenav: false
    }
  }
}
</script>

<style>
body,
html {
  font-family: "Open Sans", sans-serif;
  margin: 0;
}
</style>
