<template>
  <footer class="text-center">
      <div id="footer-top" class="container clearfix py-5">
          <div class="float-start">
              <img src="../img/avadabarbers_footer_shop_image-400x312.png" alt="Shop">
              <button class="my_btn">Shop our range now</button>
          </div>
          <div class="float-start">
                <img src="../img/avadabarbers-logo-x2-200x70.png" alt="Logo" class="pt-4 mb-5">
                <span class="d-block">{{item.name}}</span>
                <span class="d-block">{{item.address}}</span>
                <span class="d-block">{{item.city}}</span>
                <span class="d-block">{{item.email}}</span>
                <span class="d-block mb-4">{{item.number}}</span>
                <p class="text-uppercase fw-bold mt-4">Follow us</p>
                <ul class="lisy-unstyled px-0 pt-3">
                    <li v-for="social,index in socials" :key="index" class="d-inline-block px-2 pointer"><i :class="`fab fa-${social}`"></i></li>
                </ul>
          </div>
          <div class="float-start">
              <img src="../img/avadabarbers_footer_appointment_image-400x312.png" alt="Book">
              <button class="my_btn">Book your appointment</button>
          </div>
      </div>
      <div id="footer-bottom" class="d-flex justify-content-center align-items-center position-relative">
          <p class="m-0"><i class="far fa-copyright"></i> Copyright 2012 - 2020 | Avada Theme by ThemeFusion | All Rights Reserved | Powered by WordPress</p>
          <button class="border-0 rounded-top p-3 d-flex align-items-center"><i class="fas fa-chevron-up"></i></button>
      </div>
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
@import '../my_common_styles.scss';
    footer {
        background: #000000;

        #footer-top {
            div {
                width: calc(100%/3);
                object-fit: contain;

                span {
                    color: $lightgrey;
                }

                p {
                    color: $goldish;
                }

                li {
                    color: $lightgrey;
                }
            }
        }

        #footer-bottom {
            height: 100px;
            color: $grey;
            background: #161718;

            button {
                height: 30px;
                position: absolute;
                bottom: 0;
                right: 5%;
                color: $lightgrey;
                background: #303030;
            }
        }
    }
</style>