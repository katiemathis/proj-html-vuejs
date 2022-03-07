<template>
    <!-- inizio newsletter and subscribe section -->
    <div class="subscribe_container">
        <div class="col-8 m-auto">
            <div class="row subscribe_text">
                <div class="col">
                    <h3>Subscribe to our Newsletter</h3>
                </div>
            </div>
            <!-- inizio input bar section -->
            <div class="row submit_bar">
                <div class="col-8 m-auto">
                    <div class="row">
                        <!-- inizio input bar dettagli con event click -->
                        <div class="col-8">
                            <input type="text" placeholder="Insert your email*" v-model="email" @keyup.enter="subscribe()">
                        </div>
                        <!-- inizio button con event click -->
                        <div class="col-4">
                            <button class="all_caps_button" @click="subscribe()">send</button>
                        </div>

                    </div>
                    
                    
                </div>


            </div>

        </div>
        
    </div>
  
</template>

<script>

//sotto ci sono dettagli del evento
export default {
    name: 'NewsletterSubscribe',
    email: '',
    methods: {
    subscribe() {
            alert('Thank you! The email address: ' + this.email + 
            ' has been added to our Newsletter mailing list. Please check your email to confirm your subscription.')

        

        },

    }



}
</script>

<style scoped lang="scss">

@import '../../style/general.scss';

//all subscribe rules

.subscribe_container {
    background-color: $colorLightGrey;
    height: 200px;
    padding: 50px;

    .subscribe_text{
        text-align: center;
    }

    //submit bar rules

    .submit_bar {
        

        input {
            width: 100%;
            margin: 10px;
            border: 0.5px solid #e0dfdf;
            padding: 5px 10px; 
            font-size: 0.8em;
        }

        //button rules

        .all_caps_button {
            @include all_caps_button;
            background-color: $colorShark;
            color: $colorWhite;
            padding: 5px 40px;            
            margin: 10px;
            &:hover {
                color: $colorRoyalBlue;
            }
        }

    }

}



</style>