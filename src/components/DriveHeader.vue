<template>
  <header>
    
    <div id="header-top">

      <div class="container">

        <div id="row-header-top">

          <div>
            We have 95% Successful Pass Rate!
          </div>

          <div>
            <i class="fas fa-phone"></i>
            Give us a call to book yout tuition! 1-800-555-555
          </div>

        </div>

      </div>

    </div>

    <div id="header-bottom">

      <div class="container">

        <div id="row-header-bottom">

          <div class="logo-container">

            <img src="../assets/images/avada-drivers-logo-1x.png" alt="avada-logo">

          </div>

          <nav>

            <ul>

              <li v-for="navElem in navData" :key="navElem.name" :class="navElem.active ? 'active' : ''">
                {{navElem.name}}
                <span v-if="navElem.new">NEW</span>
              </li>

            </ul>

          </nav>

          <div class="btn btn-green">
            BOOK NOW
          </div>

        </div>

      </div>

    </div>

  </header>
</template>

<script>
export default {
  name: 'DriveHeader',
  
  props: {
    navData: Array
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '@/assets/scss/variables.scss';

  header {
    position: relative;
    z-index: 5;
  }

  .container {
    @include page-center
  }

  #header-top {
    background-color: #484848;
    padding: 15px 0;
    position: sticky;
    left: 0;
    top: 0;
    right: 0;

    #row-header-top {
      display: flex;
      justify-content: space-between;
      font-size: .8rem;
      color: #7f9ea8;

      i{
        margin: 0 10px;
      }
    }
  }

  #header-bottom {
    background-color: #48484878;
    padding: 30px 0;

    #row-header-bottom {
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      color: white;

      .logo-container {
        cursor: pointer;

        img {
          max-width: 100%;
        }
      }

      nav {
        min-width: 55%;
        ul {
          list-style: none;
          display: flex;
          justify-content: space-around;

          li {
            cursor: pointer;
            padding-bottom: 12px;
            display: flex;

            &.active {
              color: $greenMain;
              border-bottom: 3px solid $greenMain;
              padding-bottom: 9px;
            }

            span {
              font-size: .7rem;
              background-color: $greenMain;
              padding: 3px 7px;
              margin-left: 5px;
              border-radius: 5px;
            }
          }
        }
      }

      .btn {
        border-radius: 30px;
        padding: 12px 30px;
        cursor: pointer;
      }

      .btn-green {
        background-color: $greenMain;
      }

    }
  }
</style>
