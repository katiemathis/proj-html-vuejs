<template>
    <!-- qua c'è l'intro text per la gallery. Si può riutilizzare questa sezione 
    usando le props in caso di bisogno di replicare la sezione -->
    <div class="gallery-intro-text-container">
            <div class="col-6 m-auto">
                <div class="row gallery-intro-text">
                    <h6 class="all_caps_title">phasellus eget metus</h6>
                    <h3>All the latest news</h3>
                </div>
            <div class="col-1 m-auto orange_divider"></div>
        </div>
    </div>
  
</template>

<script>
export default {
    name: 'GalleryIntroText',

}
</script>

<style scoped lang="scss">

@import '../../style/general.scss';

//all intro text rules

.gallery-intro-text-container {
    min-height: 150px;

    .gallery-intro-text {
        color: $colorShark;
        text-align: center;
        padding: 40px 0 10px 0;
        

        .all_caps_title {
            @include all-caps-title;
        }

        h3 {
            font-weight: 700;
        }

    }

    //accent divider rules

    .orange_divider {
        width: 50px;
        height: 2px;
        background-color: $colorSalmon;
    }
}

</style>