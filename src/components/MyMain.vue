<template>
    <div class="main-container">
        <MyJumbotron />
        <div class="top-text-container">
            <div class="col-6 m-auto">
                <div class="row top-text">
                    <h6 class="all_caps_title">avada forum is the place to be</h6>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores corrupti a, numquam voluptatum illum, sapiente, commodi sit nostrum obcaecati omnis dolor non ex. Illum eum a temporibus fuga dolores libero!</p>
                </div>
            </div>
        </div>
        <div class="gallery-intro-text-container">
            <div class="col-6 m-auto">
                <div class="row gallery-intro-text">
                    <h6 class="all_caps_title">phasellus eget metus</h6>
                    <h3>All the latest news</h3>
                </div>
                <div class="col-1 m-auto orange_divider"></div>
            </div>
        </div>

    </div>
</template>

<script>
import MyJumbotron from './partials/MyJumbotron.vue'

export default {
    name: 'MyMain',
    components: {
        MyJumbotron,
    },
}
</script>

<style scoped lang="scss">

@import '../style/general.scss';

.top-text-container {
    min-height: 250px;
    background-color: $colorLightGrey;

    .top-text {
        color: $colorShark;
        text-align: center;
        padding: 50px;

        .all_caps_title {
            @include all-caps-title;
        }

    }
}
.gallery-intro-text-container {
    min-height: 250px;

    .gallery-intro-text {
        color: $colorShark;
        text-align: center;
        padding: 50px;

        .all_caps_title {
            @include all-caps-title;
        }

    }

    .orange_divider {
        width: 50px;
        height: 2px;
        background-color: $colorSalmon;
    }
}

</style>