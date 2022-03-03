<template>
    <div class="subscribe_container">
        <div class="col-8 m-auto">
            <div class="row subscribe_text">
                <div class="col">
                    <h3>Subscribe to our Newsletter</h3>
                </div>
            </div>
            <div class="row submit_bar">
                <div class="col-10 m-auto">
                    <input type="text" placeholder="Insert your email*">
                    <button class="btn all_caps_title">send</button>
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
    height: 200px;
    padding: 50px;

    .subscribe_text{
        text-align: center;
    }

    .submit_bar {
        margin-top: 20px;

        input {
            width: 350px;
            margin: 10px;
        }

        .all_caps_title {
            @include all_caps_title;
            background-color: $colorShark;
            color: $colorWhite;
            padding: 5px 40px;
            font-size: x-small;
            margin: 10px;
        }

    }


    

     
    
}



</style>