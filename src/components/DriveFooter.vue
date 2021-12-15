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

    <div class="row-footer-bottom">

      <div class="container">

        <div id="copyright">&#169; Copyright 2012 - 2020 | Avada Theme by <span>FLU</span> | All Right Reserved | Powered by <span>VueCLI</span></div>

        <div class="socials">

          <i class="fab fa-facebook-f"></i>
          <i class="fab fa-twitter"></i>
          <i class="fab fa-youtube"></i>
          <i class="fab fa-instagram"></i>

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

    &:hover {
      background-color: white;
      color: $greenMain;
      border: solid 3px $greenMain;
    }
  }

  .row-footer-top {
    background-image: url("../assets/images/footer-background-color.jpg");
    background-size: cover;
    background-position: center;
    color: rgb(175, 175, 175);
    padding: 50px 0;
    
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
      .logo-info{
        p {
          line-height: 30px;
        }
        img {
          max-width: 100%;
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
          li {
            cursor: pointer;
          }
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

  .row-footer-bottom {
    background-color: #1c1d1e;
    color: grey;
    padding: 50px 0;

    .container {
      display: flex;
      justify-content: space-between;

      #copyright {
        font-size: .8rem;
        span {
          color: $greenMain;
          cursor: pointer;
        }
      }

      .socials {
        i {
          color: white;
          margin: 0 10px;
          cursor: pointer;
        }
      }
    }
  }

</style>