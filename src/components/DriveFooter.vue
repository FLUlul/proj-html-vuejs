<template>
  <footer>
    <div class="row-footer-top">

      <div class="container">

        <div class="logo-info col">

          <img src="../assets/images/avada-drivers-logo-1x.png" alt="logo avada footer">

          <p>Avada Driving School is the right choice for experienced drivers looking for a refresher course, or the brand new driver wanting to pass first time.</p>

        </div>

        <nav class="contacts-footer col">

          <div class="title-nav-footer">
            CONTACT DETAILS
          </div>

          <ul>
            <li v-for="contact in navContacts" :key="contact.contact">

              <i :class="contact.logo"></i>

              {{contact.contact}}

            </li>
          </ul>

        </nav>

        <nav class="courses-footer col">

          <div class="title-nav-footer">
            COURSES
          </div>

          <ul>
            <li v-for="course in navCourses" :key="course.course">

              <i :class="course.logo"></i>

              {{course.course}}

            </li>
          </ul>

        </nav>

        <div class="rate-book col">

          <div class="img-container">

            <img src="../assets/images/footer-ad-grid.png" alt="footer rates">

          </div>

          <div class="btn btn-green">BOOK NOW</div>

        </div>

      </div>

    </div>
  </footer>
</template>

<script>
export default {
  name: 'DriveFooter',
  props: {
    navContacts: Array,
    navCourses: Array,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '@/assets/scss/variables.scss';
  /* global */
 .container {
    @include page-center;
  }
  .btn {
    @include button-standard
  }
  .btn-green {
    background-color: $greenMain;
    color: white;
    display: inline-block;
  }

  .row-footer-top {
    background-image: url("../assets/images/footer-background-color.jpg");
    background-size: cover;
    background-position: center;
    color: rgb(175, 175, 175);
    padding: 50px 0;

    .logo-info{
      p {
        line-height: 30px;
      }
      img {
        max-width: 100%;
      }
    }
    
    .container {
      display: flex;

      .col {
        width: calc(100% / 4);
        padding: 25px;
        ul {
          list-style: none;
          li {
            margin: 20px 0;
          }
        }
        .title-nav-footer {
          color: white;
          font-weight: 600;
        }
      }

      .contacts-footer {
        i {
          margin-right: 10px;
        }
      }

      .courses-footer {
        ul {
          color: $greenMain;
          i {
            margin: 5px 5px;
          }
        }
      }

      .rate-book {
        text-align: center;
          .img-container {
          width: 100%;
          margin-bottom: 15px;
          img {
            max-width: 100%;
          }
        }
      }
    }
  }

</style>