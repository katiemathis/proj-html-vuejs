<template>
    <div class="top-text-container">
        <div class="col-6 m-auto">
            <div class="row top-text">
                <h6 class="all_caps_title">avada forum is the place to be</h6>                    
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                    Maiores corrupti a, numquam voluptatum illum, sapiente, 
                    commodi sit nostrum obcaecati omnis dolor non ex. 
                    </p>
            </div>
        </div>
    </div>
  
</template>

<script>
export default {
    name: 'TopText',
}
</script>

<style scoped lang="scss">

@import '../../style/general.scss';

.top-text-container {
    min-height: 200px;
    background-color: $colorLightGrey;

    .top-text {
        color: $colorShark;
        text-align: center;
        padding: 50px;

        .all_caps_title {
            @include all-caps-title;
        }

            p {
                color: $colorNevada;
                font-weight: 200;
                font-size: 1.5em;
            }

    }
}

</style>