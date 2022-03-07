<template>
  <!-- standard call to action striscia nera con testo bianco che viene popolato in modo dinamico con i dati da main -->
  <div class="cta_container">
      <div class="col-6 m-auto cta_text">
          <div class="row">
            <h6 class="all_caps_title">{{cta}} <span> <i class="fa-solid fa-right-long"></i></span></h6>
          </div>
      </div>
  </div>
</template>

<script>

//cta = "call to action" -- i dati si trovano all'interno di main.vue
export default {
    name: 'CallToAction',
    props: {
        'cta': String  
    }

}
</script>

<style scoped lang="scss">

@import '../../style/general.scss';

//all cta rules

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
                text-transform: uppercase;
                font-size: 0.8em;
                font-weight: 700;
                line-height: 90px;
                &:hover {
                    cursor: pointer;
                    color: $colorSalmon;
                }

                span {
                    padding-left: 10px;
                }
            }
        }
    }
}

</style>