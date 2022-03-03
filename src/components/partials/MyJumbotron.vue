<template>
    <div class="jumbotron-container">
        <div class="col-8 m-auto">
            <div class="row jumbotron-contents">
                <h1>Tech Forum!</h1>
                <p>Discuss all the latest technology and trends</p>
                <div class="col">
                <button class="btn get_avada_button">GET AVADA NOW</button>
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

.jumbotron-container {
    min-height: 500px;
    background-image: url('../../assets/images/home_slider_bg.jpg');
    background-size: cover;

    .jumbotron-contents {
        color: $colorWhite;
        vertical-align: middle;
        transform: translateY(80%);
        font-size: xx-large;
        
        .get_avada_button {
            background-color: $colorEasternBlue;
            color: $colorWhite;
        }
    }
}

</style>