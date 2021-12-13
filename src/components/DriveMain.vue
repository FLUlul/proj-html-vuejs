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

    <section id="free-lesson">

      <div class="container">
        
        <div class="row-lesson">

          <div class="lesson-lx">
            <h2>Get Behind The Wheel</h2>

            <p class="lesson-sub-title">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eligendi minima veniam obcaecati incidunt
            </p>

            <p class="lesson-para">
              Lorem ipsum dolor, sit amet consectetur adipisicing elit. Mollitia ullam quia, aliquam eius maiores omnis, modi a sequi ab dolorem laboriosam! Quod dolores ratione dolore repudiandae autem consequatur, fugiat nemo optio cum, ipsum quae neque animi numquam, dolorum recusandae totam eveniet!
            </p>
          </div>

          <div class="lesson-rx">

            <div class="from-container">

              <div class="title">
                <h3>
                  First Lesson Free!
                </h3>

                <div>
                  When you make a block booking with us your first lesson is included free.
                </div>
              </div>

              <form action="#">

                <input type="text" placeholder="Your Name*">

                <input type="text" placeholder="Email*">

                <input type="text" placeholder="Telephone">

                <input type="text" placeholder="Location">

                <div class="btn btn-green">REQUEST A CALLBACK</div>
              </form>

            </div>

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
    display: flex;
    align-items: center;
    height: 700px;
    background-image: url("../assets/images/homepage-hero-background.jpg");
    background-size: 110%;
    background-repeat: no-repeat;
    background-position: center;
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

  #free-lesson {
    margin-top: 540px;

    .row-lesson {
      display: flex;
      padding: 50px 0 150px;

      .lesson-lx {
        width: 50%;
        color: $greyMain;
        padding: 0 15px;

        h2 {
          margin: 15px 0;
          font-size: 2.7rem;
        }

        p {
          margin: 50px 0;
        }
        .lesson-sub-title {
          font-size: 1.5rem;
          line-height: 2rem;
        }
        .lesson-para {
          font-size: 1.2rem;
          line-height: 1.7rem;
        }
      }

      .lesson-rx {
        width: 50%;
        text-align: center;
        position: relative;

        .from-container{
          padding: 40px;
          box-shadow: 0px 25px 50px -20px grey;
          border-radius: 20px;
          position: absolute;
          background-color: #ffff;
          top: -120px;

          .title{
            
            h3 {
              font-size: 2rem;
              color: $greenMain;
              margin-bottom: 50px;
            }

            div {
              color: $greyMain;
              margin: 25px 0;
              line-height: 25px;
            }
          }

          form{

            input {
              width: 100%;
              padding: 13px;
              border: solid rgb(197, 197, 197) 1px;
              border-radius: 5px;
              background-color: #f7f7f7;
              margin: 20px 0;
            }

            input:nth-child(1) {
              background-image: url("../assets/images/image.png");
              background-repeat: no-repeat;
              background-position-x: 98%;
              background-position-y: 50%;
            }

            .btn {
              @include button-standard;
              width: 50%;
              margin: 25px auto;
            }
            .btn-green {
              color: white;
              background-color: $greenMain;
            }
          }
        }  
      }
    }
  }
  
</style>