<template>
    <div class="main-container">
        <MyJumbotron />
        <TopText />
        <GalleryIntroText />
        <MyGallery />
        <FeaturedArticle />
        <MyGallery />
        <ReviewedAndTutorials />
        <CallToAction />
        <ForumsIntroText />
        <ForumSections />
        <CallToAction />
        
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
        NewsletterSubscribe
    },
}
</script>

<style scoped lang="scss">

@import '../style/general.scss';




</style>