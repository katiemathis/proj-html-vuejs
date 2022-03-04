<template>
    <div class="main-container">
        <MyJumbotron />
        <TopText />
        <GalleryIntroText />
        <div class="gallery-container">
            <div class="col-8 m-auto gallery">
                <div class="row row-cols-3 g-4">
                    <MyGallery :galleryOneItems="galleryOneItems" :item="item" 
                    v-for="(item, index) in galleryOneItems" :key="index"/>
                </div>
            </div>
        </div>
        <FeaturedArticle />
        <div class="gallery-container">
            <div class="col-8 m-auto gallery">
                <div class="row row-cols-3 g-4">
                    <MyGallery :galleryTwoItems="galleryTwoItems" :item="item" 
                    v-for="(item, index) in galleryTwoItems" :key="index"/>
                </div>
            </div>
        </div>
        <ReviewedAndTutorials />
        <CallToAction :cta="cta1" />
        <ForumsIntroText />
        <ForumSections />
        <CallToAction :cta="cta2" />
        <MySlider />
        <NewsletterSubscribe />

    </div>
</template>

<script>
import MyJumbotron from './partials/MyJumbotron.vue'
import TopText from './partials/TopText.vue'
import MyGallery from './partials/MyGallery.vue'
import GalleryIntroText from './partials/GalleryIntroText.vue'
import FeaturedArticle from './partials/FeaturedArticle.vue'
import ReviewedAndTutorials from './partials/ReviewedAndTutorials.vue'
import CallToAction from './partials/CallToAction.vue'
import ForumsIntroText from './partials/ForumsIntroText.vue'
import ForumSections from './partials/ForumSections.vue'
import MySlider from './partials/MySlider.vue'
import NewsletterSubscribe from './partials/NewsletterSubscribe.vue'


export default {
    name: 'MyMain',
    components: {
        MyJumbotron,
        MyGallery,
        TopText,
        GalleryIntroText,
        FeaturedArticle,
        ReviewedAndTutorials,
        CallToAction,
        ForumsIntroText,
        ForumSections,
        MySlider,
        NewsletterSubscribe
    },
    data () {
        return {
            cta1: 'Read Our Blog',
            cta2: 'Go to Our Forum',
            galleryOneItems : [
                {
                    url:'../../img/post_feat_img_25-320x202.jpg',
                    date: 'October 11 | 2 comments',
                    name:'This is a Title',
                    text: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Et temporibus voluptatum suscipit tempore aliquid deleniti aut veniam inventore eligendi ex ad ullam, cumque provident totam omnis, magnam dolores dolorum corporis.'
                },
                {
                    url:'../../img/post_feat_img_24-320x202.jpg',
                    date: 'October 11 | comments off',
                    name:'This is a Title',
                    text: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Et temporibus voluptatum suscipit tempore aliquid deleniti aut veniam inventore eligendi ex ad ullam, cumque provident totam omnis, magnam dolores dolorum corporis.'
                },
                {
                    url:'../../img/post_feat_img_23-320x202.jpg',
                    date: 'October 11 | 2 comments',
                    name:'This is a Title',
                    text: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Et temporibus voluptatum suscipit tempore aliquid deleniti aut veniam inventore eligendi ex ad ullam, cumque provident totam omnis, magnam dolores dolorum corporis.'
                },

            ],
            galleryTwoItems : [
                {
                    url:'../../img/post_feat_img_22-320x202.jpg',
                    date: 'October 11 | 2 comments',
                    name:'This is Another Title',
                    text: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Et temporibus voluptatum suscipit tempore aliquid deleniti aut veniam inventore eligendi ex ad ullam, cumque provident totam omnis, magnam dolores dolorum corporis.'
                },
                {
                    url:'../../img/post_feat_img_21-320x202.jpg',
                    date: 'October 11 | comments off',
                    name:'This is Another Title',
                    text: 'This is some text from the article. This is some more text from the article. More text.'
                },
                {
                    url:'../../img/post_feat_img_20-320x202.jpg',
                    date: 'October 11 | comments off',
                    name:'This is Another Title',
                    text: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Et temporibus voluptatum suscipit tempore aliquid deleniti aut veniam inventore eligendi ex ad ullam, cumque provident totam omnis, magnam dolores dolorum corporis.'
                },

            ]
        }
    }
}
</script>

<style scoped lang="scss">

@import '../style/general.scss';

.gallery-container {
    margin: 10px 0;
    padding: 10px 0;
}




</style>