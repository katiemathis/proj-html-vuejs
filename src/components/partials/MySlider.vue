<template>
    <!-- inizio slider -->
    <div class="slider_container">
        <div class="col-4 m-auto">
            <div class="row">
                <div class="col join_contents">
                    <h1 class="join_title">Hey! Join our Community</h1>
                    <p class="join_text">Lorem ipsum dolor sit, amet consectetur adipisicing elit. 
                        Cumque nemo deleniti voluptatum aliquam libero nobis a ipsam vel repellendus.</p>
                    <button class="all-caps-button">Sign up<span><i class="fa-solid fa-angle-right"></i></span></button>
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

//all slider rules

.slider_container {
    min-height: 300px;
    background-image: url('../../assets/images/join_now_cta_bg.jpg');
    background-size: cover;
    color: $colorWhite;
    text-align: center;

    .join_contents {
        padding: 50px 20px;

        .join_title {
            font-size: 50px;
            font-weight: 700;
        }


        .join_text{
            font-size: small;
        }

        .all-caps-button {
            @include all-caps-button;
            background-color: $colorEasternBlue;
            color: $colorWhite;
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