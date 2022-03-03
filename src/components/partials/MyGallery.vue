<template>
  <div class="gallery-container">
      <div class="col-8 m-auto gallery">
          <div class="row">
              <div class="col article_card">
                  <img src="../../assets/images/post_feat_img_23-147x118.jpg" alt="">
                  <h6>Title</h6>
                  <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Maxime eum porro ab dicta repudiandae hic, non minima pariatur magnam ut exercitationem veniam deserunt reprehenderit, deleniti corporis ipsum, odit iste dolore!</p>
              </div>
              <div class="col article_card">
                  <img src="../../assets/images/post_feat_img_23-147x118.jpg" alt="">
                  <h6>Title</h6>
                  <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Maxime eum porro ab dicta repudiandae hic, non minima pariatur magnam ut exercitationem veniam deserunt reprehenderit, deleniti corporis ipsum, odit iste dolore!</p>
              </div>
              <div class="col article_card">
                  <img src="../../assets/images/post_feat_img_23-147x118.jpg" alt="">
                  <h6>Title</h6>
                  <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Maxime eum porro ab dicta repudiandae hic, non minima pariatur magnam ut exercitationem veniam deserunt reprehenderit, deleniti corporis ipsum, odit iste dolore!</p>
              </div>
          </div>
      </div>

  </div>
</template>

<script>
export default {
    name: 'MyGallery',

}
</script>

<style scoped lang="scss">
@import '../../style/general.scss';

.article_card {
    max-height: 300px;
    max-width: 400px;
    overflow: hidden;

    img {
        width: 100%;
        object-fit: cover;
    }

    h6 {
        margin-top: 10px;
    }

    p {
        font-size: 10px;
        padding-right: 10px;
        
    }

}

</style>