<template>
    <header id="top" class="position-relative pt-3 pb-5">
        <div class="container">
            <!-- Top bar -->
            <nav class="navbar navbar-dark">
                <div class="container-fluid">
                    <img src="../img/avadabarbers-logo-x1.png" alt="Logo" class="pointer">
                    <div class="d-flex align-items-center">
                        <a href="#main-2"><i class="fas fa-shopping-cart"></i></a>
                        <button class="navbar-toggler border-0" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
                            <span class="navbar-toggler-icon"></span>
                        </button>
                    </div>
                    <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
                        <div class="navbar-nav">
                            <a v-for="voice,index in item" :key="index" class="nav-link active text-end" aria-current="page" :href="`#main-${index}`" style="color: $lightestgrey">{{voice}}</a>
                        </div>
                    </div>
                </div>
            </nav>
            <!-- /Top bar -->

            <div id="jumbotron" class="container d-flex justify-content-around align-items-center px-5">
                <div>
                    <h1>Barber Shop</h1>
                    <hr>
                    <p class="fs-3 grey-p">The Pinnacle of Male Grooming</p>
                    <button class="my_btn goldish_btn mt-5">Learn More</button>
                </div>
                <img src="../img/avadabarbers_hero_focalmirror-600x825.png" alt="Cutting hair" class="not_scale">
            </div>
        </div>

        <!-- Top right fixed buttons -->
        <div id="buttons">
            <button id="demos" class="white_btn pointer d-block border-0 rounded-3 mb-1">
                <i class="fas fa-3x fa-folder-plus"></i>
                <p>Demos</p>
            </button>
            <button id="sale" class="white_btn pointer border-0 rounded-3">
                <i class="fas fa-dollar-sign"></i>
                <span class="fs-3 fw-bold">39</span>
                <p>On Sale</p>
            </button>
        </div>
        <!-- /Top right fixed buttons -->
    </header>
</template>

<script>
export default {
    name: 'Header',
    props: {
        item: Array
    }
}
</script>

<style lang="scss">
@import '~bootstrap/scss/bootstrap.scss';
@import '../common.scss';
@import '../responsive.scss';

header {
    background: url(../img/avadabarbers-homepage-hero-bg.jpg);

    a {
        margin-right: 10px;
        color: $lightestgrey;
        outline: none;
    }

    img {
        max-width: 65%;
    }

    #jumbotron {
        h1 {
            font-size: 100px;
            font-weight: 900;
            color: $lightestgrey;
        }

        hr {
            width: 50%;
            height: 3px;
            color: $goldish;
            opacity: 0.8;
        }

        p {
            font-weight: lighter;
            color: $grey;
        }
    }
    // Top right fixed buttons
        #buttons {
            position: fixed;
            top: 20%;
            right: 5px;
            z-index: 2;
            font-size: 14px;

            .white_btn {
            width: 70px;
            height: 70px;
            outline: none;
            color: #4a5259;
            }

            #demos {
                i {
                    color: #4f659a;
                }
            }

            #sale {
                i, span {
                    color: #83c994;
                }
                i {
                    position: relative;
                    top: -10px;
                }
            }
        }
    // --Top right fixed buttons
} 
</style>