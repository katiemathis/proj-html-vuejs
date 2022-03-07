<template>
    <!-- qua uso le props da main per poter popolare le due gallerie diverse -->
     <div class="col article_card">
        <img :src="`${item.url}`" :alt="`${item.name}`">
        <p class="article_title">{{item.name}}</p>
        <p class="article_date">{{item.date}}</p>
        <p class="article_preview">{{item.text}}</p>
    </div>

</template>

<script>

//sotto troviamo le props passate da main
export default {
    name: 'MyGallery',
    props: {
        'galleryOneItems': Array,
        'galleryTwoItems': Array,
        'item' : Object
    }

}
</script>

<style scoped lang="scss">
@import '../../style/general.scss';

//general rules

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

//article card rules

.article_card {
    max-height: 300px;
    max-width: 400px;
    overflow: hidden;
    margin: 10px 0;


    img {
        width: 100%;
        object-fit: cover;
        padding-bottom: 2px;
        border-bottom: 2px solid transparent;
        &:hover {
            border-bottom: 2px solid $colorEasternBlue;
            cursor: pointer;
        }
    }

    .article_title {
        font-size: .9em;
        margin-top: 10px;
        font-weight: 600;
        padding-top: 2px;
        
    }

    .article_date {
        font-size: .6em;
        padding-right: 10px; 
        margin-top: -15px;
    }

    .article_preview {
        font-size: .7em;
        padding-right: 10px;
        margin-top: -10px;
    }

}

</style>