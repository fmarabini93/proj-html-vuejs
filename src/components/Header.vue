<template>
    <header id="top" class="position-relative">
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
                            <a v-for="voice,index in item" :key="index" class="nav-link active text-end" aria-current="page" :href="`#main-${index}`" style="color: #8b8b8b">{{voice}}</a>
                        </div>
                    </div>
                </div>
            </nav>
            <!-- /Top bar -->


            <div id="jumbotron" class="d-flex justify-content-between align-items-center">
                <div>
                    <h1>Barber Shop</h1>
                    <hr>
                    <p class="fs-3">The Pinnacle of Male Grooming</p>
                    <button class="my_btn goldish_btn mt-5">Learn More</button>
                </div>
                <img src="../img/avadabarbers_hero_focalmirror-600x825.png" alt="Cutting hair" class="not_scale">
            </div>
        </div>

        <!-- Top right fixed buttons -->
        <div id="buttons">
            <button id="demos" class="white_btn pointer d-block border-0 rounded-3 mb-3">
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
@import '../my_common_styles.scss';

    header {
        min-height: 100vh;
        background: url(../img/avadabarbers-homepage-hero-bg.jpg);

        a {
            margin-right: 20px;
            color: $lightgrey;
            outline: none;
        }
    }

    #jumbotron {
        h1 {
            font-size: 100px;
            color: #ffffff;
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
    
</style>