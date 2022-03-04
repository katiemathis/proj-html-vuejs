<template>
     <div class="col article_card">
        <img :src="`${item.url}`" :alt="`${item.name}`">
        <p class="article_title">{{item.name}}</p>
        <p class="article_date">{{item.date}}</p>
        <p class="article_preview">{{item.text}}</p>
    </div>

</template>

<script>
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

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.article_card {
    max-height: 300px;
    max-width: 400px;
    overflow: hidden;
    margin: 10px 0;


    img {
        width: 100%;
        object-fit: cover;
        padding-bottom: 2px;
        &:hover {
            border-bottom: 2px solid $colorEasternBlue;
            cursor: pointer;
        }
    }

    .article_title {
        font-size: 12px;
        margin-top: 10px;
        font-weight: 600;
        padding-top: 2px;
        
    }

    .article_date {
        font-size: 10px;
        padding-right: 10px; 
    }

    .article_preview {
        font-size: 10px;
        padding-right: 10px;
    }

}

</style>