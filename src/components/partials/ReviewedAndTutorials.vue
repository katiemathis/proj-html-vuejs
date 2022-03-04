<template>
  <div class="container reviewed_tutorials_container col-8 m-auto">
      <div class="row">
        <div class="reviewed_product_container col-8">
            <h6 class="all_caps_title">reviewed product</h6>
                <h2>This is the Reviewed Product, isn't it cool?</h2>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                Maxime laborum, nisi autem excepturi sed, numquam sequi voluptate quos. </p>
                <div class="col-6">
                    <button class="btn read_more all_caps_title">read more > </button>
                </div>

        </div>
        <div class="tutorials_container col-4">
            <div class="row tutorial_title">
                <h5>Tutorials and Guides</h5>
                <div class="col-1 orange_divider"></div>
            </div>
            <div class="row tutorial_tiles">
                <div class="col-5">
                    <img src="../../assets/images/post_feat_img_23-147x118.jpg" alt="">
                </div>
                <div class="col-7">
                    <p>Description of reviewed product</p>
                </div>
            </div>
            <div class="row row-3 tutorial_tiles">
                <div class="col-5">
                    <img src="../../assets/images/post_feat_img_22-147x118.jpg" alt="">
                </div>
                <div class="col-7">
                    <p>Description of reviewed product</p>
                </div>
            </div>
            <div class="row tutorial_tiles">
                <div class="col-5">
                    <img src="../../assets/images/post_feat_img_20-147x118.jpg" alt="">
                </div>
                <div class="col-7">
                    <p>Description of reviewed product</p>
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

.reviewed_tutorials_container {
    margin: 10px;

    .reviewed_product_container {
        margin: 20px 0;
        height: 300px;
        background-image: url('../../assets/images/featured_article_2_bg.jpg');
        background-size: cover;
        color: $colorWhite;
        font-size: x-small;
        padding: 50px;

        .all_caps_title {
            @include all-caps-title;
        }

        .read_more {
            background-color: $colorShark;
            color: $colorWhite;
            padding: 10px 30px;
        }
        
    }

    .tutorials_container {
        margin: 20px 0;
        padding: 0 30px;

        .orange_divider {
        width: 50px;
        height: 2px;
        background-color: $colorSalmon;
        margin: 5px 15px;
        }

        .tutorial_tiles {
            max-height: 90px;
            margin-top: 10px;
            
            img {
                width: 90px;
                object-fit: cover;
            }

            p {
                font-size: xx-small;

            }
        }

    }
}

</style>