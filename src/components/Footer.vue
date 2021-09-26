<template>
  <div>
    <!-- Footer Section -->
    <footer>
        <section id="foot">
          <div class="my-view">
            <button class="btn-su">SIGN-UP NOW!</button>
            <div class="social-section">
              <h3>FOLLOW US</h3>
              <img src="../assets/img/footer-facebook.png" alt="Facebook icon">
              <img src="../assets/img/footer-twitter.png" alt="Twitter icon">
              <img src="../assets/img/footer-youtube.png" alt="You Tube icon">
              <img src="../assets/img/footer-pinterest.png" alt="Pinterest icon">
              <img src="../assets/img/footer-periscope.png" alt="Periscope icon">
            </div>
          </div>
        </section>
    </footer>
    <!--/ Footer Section -->
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';
  #foot{
    background-color: $footerBgColor;
    height: 100px;
    z-index: 99;
    position: relative;
    .my-view{
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 100%;
      .btn-su{
        border: 3px solid $primaryColor;
        padding: 10px;
        color: white;
        background-color: transparent;
      }
      .social-section{
        color: white;
        display: flex;
        justify-content: space-between;
        align-items: center;
        img{
          padding-left:15px;
        }
      }
    }
  }
</style>