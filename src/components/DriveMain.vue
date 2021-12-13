<template>
  <main>
    <section id="jumbo-top">

      <div class="container">

        <div class="row-jumbo">

        <h1>
          Drive with Avada
        </h1>

        <div>
          We offer the finest driving tuition money can buy.
        </div>

        </div>

      </div>

    </section>
  </main>
</template>

<script>
export default {
  name: 'DriveMain',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '@/assets/scss/variables.scss';
 .container {
    @include page-center;
  }

  #jumbo-top {
    background-image: url("../assets/images/homepage-hero-background.jpg");
    background-size: 110%;
    background-repeat: no-repeat;
    background-position: center;
    padding: 350px 0 250px;
    color: white;
    position: absolute;
    left: 0;
    top: 0;
    right: 0;

    h1 {
      font-size: 4rem;
      margin: 20px 0;
    }
    div {
      font-size: 1.5rem;
    }
  }

</style>