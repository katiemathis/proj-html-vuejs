<template>
    <!-- inizio forums intro text -- può essere riusato se si utilizzano 
    le props da main per popolare il testo in caso ci fosse bisogno -->
    <div class="forum-intro-text-container">
            <div class="col-6 m-auto">
                <div class="row forum-intro-text">
                    <h6 class="all_caps_title">phasellus eget metus</h6>
                    <h3>Forum Sections</h3>
                </div>
            <div class="col-1 m-auto orange_divider"></div>
        </div>
    </div>
  
</template>

<script>
export default {
    name: 'ForumsIntroText',

}
</script>

<style scoped lang="scss">

@import '../../style/general.scss';


//all intro text rules
.forum-intro-text-container {
    min-height: 150px;
    background-color: $colorLightGrey;

    .forum-intro-text {
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