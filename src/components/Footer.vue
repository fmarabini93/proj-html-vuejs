<template>
  <footer class="text-center">
      <!-- Info -->
      <div id="footer-top" class="container py-5">
        <div class="row">
                <div class="col-12 col-lg-4">
                    <img src="../img/avadabarbers_footer_shop_image-400x312.png" alt="Shop">
                    <button class="my_btn goldish_btn mt-4">Shop our range now</button>
                </div>
            <div class="col-12 col-lg-4">
                <img src="../img/avadabarbers-logo-x2-200x70.png" alt="Logo" class="pt-4 mb-5">
                <span class="d-block grey-p">{{item.name}}</span>
                <span class="d-block grey-p">{{item.address}}</span>
                <span class="d-block grey-p">{{item.city}}</span>
                <span class="d-block grey-p">{{item.email}}</span>
                <span class="d-block grey-p mb-4">{{item.number}}</span>
                <p class="text-uppercase fw-bold mt-4">Follow us</p>
                <ul class="lisy-unstyled px-0 pt-3">
                    <li v-for="social,index in socials" :key="index" class="d-inline-block px-2 pointer"><i :class="`fab fa-${social}`"></i></li>
                </ul>
            </div>
            <div class="col-12 col-lg-4">
                <img src="../img/avadabarbers_footer_appointment_image-400x312.png" alt="Book">
                <button class="my_btn goldish_btn mt-4">Book your appointment</button>
            </div>
        </div>
      </div>
      <!-- /Info -->

      <!-- Credits -->
      <div id="footer-bottom" class="d-flex justify-content-center align-items-center position-relative">
            <p class="m-0 grey-p"><i class="far fa-copyright"></i> Copyright 2012 - 2020 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress</p>
            <a href="#top"><i class="fas fa-chevron-up"></i></a>
      </div>
      <!-- /Credits -->
  </footer>
</template>

<script>
export default {
    name: 'Footer',
    data() {
        return {
            socials: ["facebook-f","twitter","youtube","instagram"]
        }
    },
    props: {
        item: Object
    }
}
</script>

<style lang="scss">
@import '../common.scss';
@import '../responsive.scss';
    footer {
        background: #111110;

        // Info
            #footer-top {
                    span {
                        color: $grey;
                    }

                    p {
                        color: $goldish;
                        opacity: 0.7;
                    }

                    li {
                        color: $lightgrey;
                    }
            }
        // --Info

        // Credits
            #footer-bottom {
                height: 100px;
                background: #161718;

                p {
                    color: $darkgrey;
                }

                a {
                    width: 40px;
                    height: 30px;
                    line-height: 30px;
                    position: fixed;
                    bottom: 0;
                    right: 5%;
                    color: $lightgrey;
                    background: #303030;
                }
            }
        // --Credits    
    }
</style>