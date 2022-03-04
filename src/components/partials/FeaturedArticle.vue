<template>
    <div class="featured_article_container">
        <div class="col-8 m-auto featured_article_details">
            <div class="row featured_article_text">
                <h6 class="all_caps_title">featured article</h6>
                <h1>This is the Featured Article</h1>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                Maxime laborum, nisi autem excepturi sed, numquam sequi voluptate quos iusto, 
                iure aut aliquam culpa ratione aliquid sapiente magni quisquam. 
                Tempora, excepturi.</p>
                <div class="col-6">
                    <button class="read_more all_caps_button">read more<span><i class="fa-solid fa-angle-right"></i></span></button>
                </div>
            </div>
            
        </div>

    </div>
</template>

<script>
export default {
    name: 'FeaturedArticle'

}
</script>

<style scoped lang="scss">

@import '../../style/general.scss';

.featured_article_container {
    height: 400px;
    margin: 20px 0;

    .featured_article_details{
        height: 400px;
        background-image: url('../../assets/images/featured_article_1_bg.jpg');
        background-size: cover;
        padding: 50px;
        color: $colorWhite;

        .featured_article_text {
            transform: translateY(40%);

            .all_caps_button {
                @include all_caps_button;
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

        

        



        
    }
    
}

</style>