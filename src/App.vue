<template>
  <div id="app">

    <DriveHeader
    :navData="headerData"
    />

    <DriveMain/>

    <DriveFooter
    :navContacts="footerContactsData"
    :navCourses="footerCoursesData"
    />

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
      ],
      footerContactsData: [
        {
          "contact": "12345 North Main Street, New York, NY 555555",
          "logo": "fas fa-home"
        },
        {
          "contact": "1.800.555.6789",
          "logo": "fas fa-phone"
        }, 
        {
          "contact": "info@your-domain.com",
          "logo": "far fa-envelope"
        }, 
        {
          "contact": "Theme-Fusion.com",
          "logo": "fas fa-link"
        }       
      ],
      footerCoursesData: [
        {
          "course": "Pass Plus",
          "logo": "far fa-arrow-alt-circle-right"
        },
        {
          "course": "Intensive Course",
          "logo": "far fa-arrow-alt-circle-right"
        },
        {
          "course": "Automatic",
          "logo": "far fa-arrow-alt-circle-right"
        },
        {
          "course": "Instructor Training",
          "logo": "far fa-arrow-alt-circle-right"
        },
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
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
