<template>
  <main>
    <!-- Jumbo section -->
    <section class="jumbo-section">
      <div class="my-view">
        <div class="jumbo-box">
           <img src="../assets/img/buy-comics-digital-comics.png" alt="Dc card sample">
           <span>digital comics</span>
        </div>
        <div class="jumbo-box">
           <img src="../assets/img/buy-comics-merchandise.png" alt="Dc card sample">
           <span>dc merchandise</span>
        </div>
        <div class="jumbo-box">
           <img src="../assets/img/buy-comics-shop-locator.png" alt="Dc card sample">
           <span>comic shop locator</span>
        </div>
        <div class="jumbo-box">
           <img src="../assets/img/buy-comics-subscriptions.png" alt="Dc card sample">
           <span>subscriptions</span>
        </div>
        <div class="jumbo-box">
           <img src="../assets/img/buy-dc-power-visa.svg" alt="Dc card sample">
           <span>dc power visa</span>
        </div>
         
      </div>
    </section>
    <!--/  Jumbo section -->

    <!-- main section -->
    <section class="main-section">
      <div class="my-view">
        <div class="specifics">
          <ul>
            <li><h2 class="specific-title">DC COMICS</h2></li>
            <li v-for='(link, index) in comics' :key="index"><a href="#">{{link}}</a></li>
            <li class="li-annidet"><h3 class="specific-title">SHOP</h3></li>
            <li v-for='(link, index) in shop' :key="index"><a href="#">{{link}}</a></li>
          </ul>
          <ul>
            <li><h2 class="specific-title">DC</h2></li>
            <li v-for='(link, index) in dc' :key="index"><a href="#">{{link}}</a></li>
          </ul>
          <ul>
            <li><h2 class="specific-title">SITES</h2></li>
            <li v-for='(link, index) in sites' :key="index"><a href="#">{{link}}</a></li>
          </ul>
        </div>
        <div class="max-logo"><img src="../assets/img/dc-logo-bg.png" alt="Dc max logo"></div>
      </div>
    </section>
    <!--/ main section -->

  </main>
</template>

<script>
export default {
    name: 'Main',
    data: function(){
      return{
        comics:[
          'Characters','Comics','Movies','TV','Games','Videos','News'
        ],
        shop: [
          'Shop Dc','Shop DC Collectibles'
        ],
        dc:[
          'Terms Of Use','Privacy policy (New)','Ad Choices','Advertising','Jobs','Subscriptions','Talents Workshops','Ratings','Shop Help','Contact Us'
        ],
        sites:[
          'DC','MAD Magazine','DC kids','DC Universe','DC Power Visa'
        ]
      }
    }
}
</script>

<style lang="scss" scoped>
    @import '../style/variables.scss';

    .jumbo-section{
      background-color: $primaryColor;
      padding-top: 30px;
      padding-bottom: 30px;
      z-index: 99;
        .my-view{
          display: flex;
          color: white;
          justify-content: space-between;
          img{
            width: 60px;
            z-index: 99;
          }
          .jumbo-box{
            display: flex;
            align-items: center;
            z-index: 99;
          }
          span{
            padding-left: 20px;
            text-transform: uppercase;
            font-size: 1rem;
            z-index: 99;
          }
        }
    }
    .main-section{
      background-image: url('../assets/img/footer-bg.jpg');
      background-position: center;
      background-size: cover;
      background-repeat: no-repeat;
      height: 450px;
      padding-top: 100px;
      position: relative;
      .my-view{
         display: flex;
         
        justify-content: space-between;
        .specifics{
          display: flex;
          justify-content: space-between;
        }
        .specific-title{
          color: white;
          margin-bottom: 10px;
        }
         img{
          z-index: 0;
          position: absolute;
          bottom: -20px;
          right:150px;
        

        };
        ul{
          list-style: none;
          line-height: 25px;
          margin-right: 30px;
          .li-annidet{
            padding-top: 10px;
          }
          a{
            text-decoration: none;
            color: rgba(255, 255, 255, 0.281);
          }
        }
      }
       
    }
</style>