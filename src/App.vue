<template>
  <div id="app">

    <DriveHeader
    :navData="headerData"
    />

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
          "active": true,
          "new": false
        },
        {
          "name": "ABOUT",
          "active": false,
          "new": false
        },
        {
          "name": "PRICES",
          "active": false,
          "new": false
        },
        {
          "name": "COURSES",
          "active": false,
          "new": true
        },
        {
          "name": "LOCATIONS",
          "active": false,
          "new": false
        },
        {
          "name": "BLOG",
          "active": false,
          "new": false
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
