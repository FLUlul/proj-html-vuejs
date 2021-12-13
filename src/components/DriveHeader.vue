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

        </div>

      </div>

    </div>

  </header>
</template>

<script>
export default {
  name: 'DriveHeader',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

  @mixin page-center {
    width: 60%;
    margin: 0 auto;
  }

  header {
    position: fixed;
    left: 0;
    top: 0;
    right: 0;
  }

  .container {
    @include page-center
  }

  #header-top {
    background-color: #484848;
    padding: 15px 0;

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
    padding: 25px 0;
  }
</style>
