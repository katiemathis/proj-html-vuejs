<template>

  <!-- inizio container per reviews and tutorials -->
  <div class="container reviewed_tutorials_container col-8 m-auto">
      <div class="row">
        <!-- inizio featured reviewed product -->
        <div class="reviewed_product_container col-8">
            <h6 class="all_caps_title">reviewed product</h6>
                <h2>This is the Reviewed Product, isn't it cool?</h2>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                Maxime laborum, nisi autem excepturi sed, numquam sequi voluptate quos. </p>
                <div class="col-6">
                    <button class="read_more all_caps_button">read more<span><i class="fa-solid fa-angle-right"></i></span></button>
                </div>

        </div>
        <!-- inizio thumbnails per reviews and tutorials -->
        <div class="tutorials_container col-4">
            <div class="row tutorial_title">
                <h5>Tutorials and Guides</h5>
                <div class="col-1 orange_divider"></div>
            </div>
            <!-- thumbnail images + text -->
            <div class="row tutorial_tiles">
                <div class="col-5">
                    <img src="../../assets/images/post_feat_img_23-147x118.jpg" alt="">
                </div>
                <div class="col-7 text">
                    <p class="description_title">Here's a cool product</p>
                    <p class="description"> October 11th, 2015 | Comments Off</p>
                </div>
            </div>
            <div class="row row-3 tutorial_tiles">
                <div class="col-5">
                    <img src="../../assets/images/post_feat_img_22-147x118.jpg" alt="">
                </div>
                <div class="col-7 text">
                    <p class="description_title">Here's another cool product. Cool, right?</p>
                    <p class="description">October 11th, 2015 | Comments Off</p>
                </div>
            </div>
            <div class="row tutorial_tiles">
                <div class="col-5">
                    <img src="../../assets/images/post_feat_img_20-147x118.jpg" alt="">
                </div>
                <div class="col-7 text">
                    <p class="description_title">This amazing product will change the world</p>
                    <p class="description">October 11th, 2015 | Comments Off</p>
                </div>
            </div>
        </div>
      </div>

  </div>
</template>

<script>
export default {
    name: 'ReviewedAndTutorials',

}
</script>

<style scoped lang="scss">

@import '../../style/general.scss';

//all reviewed and tutorials rules

.reviewed_tutorials_container {
    margin: 10px;

    //featured product rules

    .reviewed_product_container {
        margin: 20px 0;
        height: 350px;
        background-image: url('../../assets/images/featured_article_2_bg.jpg');
        background-size: cover;
        color: $colorWhite;
        font-size: small;
        padding: 60px;

        .all_caps_title {
            @include all-caps-title;
        }

        .all_caps_button {
            @include all-caps-button;
            &:hover {
                color: $colorEasternBlue;
            }

            span {
                padding-left: 10px;
            }
        }

        .read_more {
            background-color: $colorShark;
            color: $colorWhite;
            padding: 10px 30px;
        }
        
    }

    //thumbnail gallery rules 

    .tutorials_container {
        margin: 20px 0;
        //padding: 0 30px;

        .orange_divider {
        width: 50px;
        height: 2px;
        background-color: $colorSalmon;
        margin: 5px 15px;
        }

        .tutorial_tiles {
            max-height: 90px;
            margin: 10px 0 2px 0;
            overflow: hidden;

            
            img {
                height: 90px;
                max-width: 110%;
                object-fit: cover;
                border-bottom: 2px solid transparent;
                &:hover {
                    border-bottom: 2px solid $colorEasternBlue;
                    cursor: pointer;
                }
            }
            .text {
                padding-bottom: 10px;

                .description_title {
                    font-size: 0.8em;
                    font-weight: 600;
                    padding: 0;
                    margin: 0;
                }

                .description {
                    font-size: 0.6em;
                    padding: 0;
                    margin: 0;
                    
                }
            }

        }

    }
}

</style>