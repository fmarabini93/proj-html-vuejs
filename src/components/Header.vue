<template>
  <header class="position-relative">
        <div class="container">
            <nav class="d-flex justify-content-between align-items-center py-3">
                <div id="logo">
                    <img src="../img/avadabarbers-logo-x1.png" alt="Barber Logo">
                </div>
                <div id="menu">
                    <i class="fas fa-shopping-cart"></i>
                    <i class="fas fa-bars"></i>
                </div>
            </nav>
            <div id="jumbotron" class="d-flex justify-content-between align-items-center">
                <div>
                    <h1>Barber Shop</h1>
                    <hr>
                    <p>The Pinnacle of Male Grooming</p>
                    <img src="../img/hover-button.png" alt="Learn more button">
                </div>
                <img src="../img/avadabarbers_hero_focalmirror-600x825.png" alt="Cutting hair">
            </div>
        </div>
        <div id="buttons">
            <button id="demos" class="white_btn">
                <i class="fas fa-3x fa-folder-plus"></i>
                <p>Demos</p>
            </button>
            <button id="sale" class="white_btn">
                <i class="fas fa-dollar-sign"></i>
                <span class="fs-3 fw-bold">39</span>
                <p>On Sale</p>
            </button>
        </div>
  </header>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style lang="scss">
@import '~bootstrap/scss/bootstrap.scss';
@import '../variables.scss';

    header {
        height: 100vh;
        background: url(../img/avadabarbers-homepage-hero-bg.jpg);
    }
    
    #menu {
        i {
        margin-right: 10px;
        color: #ffffff;
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
            font-size: 30px;
            font-weight: lighter;
            color: $grey;
        }
    }

    #buttons {
        position: absolute;
        top: 20%;
        right: 10px;
        font-size: 14px;

        .white_btn {
        width: 70px;
        height: 70px;
        display: block;
        margin: 10px 0;
        border: none;
        border-radius: 7px;
        outline: none;
        cursor: pointer;
        color: #4a5259;
        }

        #demos {
            i {
                color: #33475B;
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
</style>