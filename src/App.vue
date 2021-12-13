<template>
  <div id="app">

    <DriveHeader/>

    <DriveMain/>

    <DriveFooter/>

  </div>
</template>

<script>
import DriveHeader from './components/DriveHeader.vue'
import DriveMain from './components/DriveMain.vue'
import DriveFooter from './components/DriveFooter.vue'

export default {
  name: 'App',
  components: {
    DriveHeader,
    DriveMain,
    DriveFooter
  },

  data() {
    return {
      headerData: [
        {
          "name": "HOME",
        },
        {
          "name": "ABOUT",
        },
        {
          "name": "PRICES",
        },
        {
          "name": "COURSES",
        },
        {
          "name": "LOCATIONS",
        },
        {
          "name": "BLOG",
        }        
      ]
    }
  }
}
</script>

<style lang="scss">
@import '~@fortawesome/fontawesome-free/css/all.min.css';
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
