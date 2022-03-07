<template>
    <!-- inizio jumbotron -->
    <div class="jumbotron-container">
        <div class="col-8 m-auto">
            <div class="row jumbotron-contents">
                <h1 class="jumbotron_title">Tech Forum!</h1>
                <p class="jumbotron_subtitle">Discuss all the latest technology news and trends</p>
                <div class="col">
                <button class="get_avada_button">GET AVADA NOW!<span><i class="fa-solid fa-angle-right"></i></span></button>
                </div>
            </div>

        </div>

    </div>
  
</template>

<script>
export default {

}
</script>

<style scoped lang="scss">

@import '../../style/general.scss';

//all jumbotron rules

.jumbotron-container {
    min-height: 450px;
    background-image: url('../../assets/images/home_slider_bg.jpg');
    background-size: cover;

    .jumbotron-contents {
        color: $colorWhite;
        vertical-align: middle;
        transform: translateY(50%);
        font-size: xx-large;

        .jumbotron_title {
            font-size: 95px;
            font-weight: 700;
        }

        .jumbotron_subtitle {
            font-size: 16px;
            font-weight: 400;
        }
        
        .get_avada_button {
            @include all_caps_button;
            background-color: $colorEasternBlue;
            font-size: 12px;
            font-weight: 700;
            &:hover {
                color: $colorSalmon;
            }

            span {
                padding-left: 10px;
            }
        }
    }
}

</style>