<template>
  <div class="cta_container">
      <div class="col-6 m-auto cta_text">
          <div class="row">
            <h6 class="all_caps_title">{{cta}} <span> <i class="fa-solid fa-right-long"></i></span></h6>
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name: 'CallToAction',
    props: {
        'cta': String  
    }

}
</script>

<style scoped lang="scss">

@import '../../style/general.scss';

.cta_container {
    background-color: $colorShark;
    min-height: 80px;
    color: $colorWhite;

    .cta_text {
        text-align: center;

            .row {
            justify-content: center;
            align-items: center;


            .all_caps_title {
                @include all-caps-title;
                line-height: 90px;
                &:hover {
                    cursor: pointer;
                    color: $colorSalmon;
                }
            }
        }
    }
}

</style>