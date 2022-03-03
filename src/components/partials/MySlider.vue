<template>
    <div class="slider_container">
        <div class="col-4 m-auto">
            <div class="row">
                <div class="col join_text">
                    <h1>Hey! Join our Community</h1>
                    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. 
                        Cumque nemo deleniti voluptatum aliquam libero nobis a ipsam vel repellendus.</p>
                    <button class="btn all-caps-title">Sign up ></button>
                </div>
            </div>
        </div>

    </div>
  
</template>

<script>
export default {
    name: 'MySlider'

}
</script>

<style scoped lang="scss">

@import '../../style/general.scss';

.slider_container {
    min-height: 300px;
    background-image: url('../../assets/images/join_now_cta_bg.jpg');
    background-size: cover;
    color: $colorWhite;
    text-align: center;

    .join_text {
        padding: 50px 20px;

        p{
            font-size: small;
        }

        .all-caps-title {
            @include all-caps-title;
            background-color: $colorEasternBlue;
            color: $colorWhite;
        }

    }
    
}

</style>