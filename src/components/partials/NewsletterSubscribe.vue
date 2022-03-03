<template>
    <div class="subscribe_container">
        <div class="col-6 m-auto">
            <div class="row">
                <h3>Subscribe to our Newsletter</h3>
                <div class="col-9">
                    <input type="text" placeholder="Insert your email*">
                </div>
                <div class="col-3">
                    <button class="btn .all_caps_title">send</button>
                </div>

            </div>

        </div>
        
    </div>
  
</template>

<script>
export default {
    name: 'NewsletterSubscribe'

}
</script>

<style scoped lang="scss">

@import '../../style/general.scss';

.subscribe_container {
    background-color: $colorLightGrey;
}



</style>