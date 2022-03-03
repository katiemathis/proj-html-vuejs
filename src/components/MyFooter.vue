<template>
    <div class="footer_container">
        <div class="col-8 m-auto">
            <div class="row footer_lists">
                <div class="col info_text">
                    <h6 class="all_caps_title">avada tech forum</h6>
                    <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. 
                        Cumque, illo iste optio atque molestias distinctio, 
                        enim modi tempora asperiores rem voluptate, blanditiis iure! 
                        Ullam fuga earum libero voluptas, dicta excepturi.</p>
                </div>
                <div class="col menu_list">
                    <h6 class="all_caps_title">Popular Topics</h6>
                    <ul class="menu-col" v-for="(popularTopic, a) in popularTopics" :key="a">
                        <li><a href="#" target="_blank" rel="noopener">{{popularTopic}}</a></li>
                    </ul>
                </div>
                <div class="col menu_list">
                    <h6 class="all_caps_title">Recent Topics</h6>
                    <ul class="menu-col" v-for="(recentTopic, a) in recentTopics" :key="a">
                        <li><a href="#" target="_blank" rel="noopener">{{recentTopic}}</a></li>
                    </ul>
                </div>
                <div class="col menu_list">
                    <h6 class="all_caps_title">Latest Replies</h6>
                    <ul class="menu-col" v-for="(latestReply, a) in latestReplies" :key="a">
                        <li><a href="#" target="_blank" rel="noopener">{{latestReply}}</a></li>
                    </ul>
                </div>

            </div>
        </div>
        <div class="footer_bottom_container">
            <div class="col-8 m-auto">
                <div class="row footer_bottom">
                    <div class="col-9 m-auto">
                        <p class="copyright">Copyright 2012 - 2020 | Avada Theme by <a href="#">Theme Fusion</a> | All Rights Reserved | Powered by <a href="https://www.linkedin.com/in/katiepalumbo/">Katie</a></p>
                    </div>
                    <div class="col-3">
                        <div class="row">
                            <ul class="menu-row footer-right">
                                <li><a href="#" target="_blank" rel="noopener"><img src="../assets/img/footer-facebook.png" alt="facebook"></a></li>
                                <li><a href="#" target="_blank" rel="noopener"><img src="../assets/img/footer-twitter.png" alt="twitter"></a></li>            
                                <li><a href="#" target="_blank" rel="noopener"><img src="../assets/img/footer-pinterest.png" alt="pinterest"></a></li>
                                <li><a href="#" target="_blank" rel="noopener"><img src="../assets/img/footer-youtube.png" alt="youtube"></a></li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>

        </div>

    </div>












    <!--<div class="footer-bottom-banner">
        <div class="footer-left">
            <button><a href="#" id="button">SIGN UP NOW</a></button>
        </div>
        
    </div>
  </div>
</div>-->
</template>

<script>

export default {
    name: 'MyFooter',

  data () {
      return {
          shopBannerItems: [
              {
                  text: 'DIGITAL COMICS',
                  src: '../../img/buy-comics-digital-comics.png',
              },
              {
                  text: 'DC MERCHANDISE',
                  src: '../../img/buy-comics-merchandise.png',
              },
              {
                  text: 'SUBSCRIPTION',
                  src: '../../img/buy-comics-subscriptions.png',
              },
              {
                  text: 'COMIC SHOP LOCATOR',
                  src: '../../img/buy-comics-shop-locator.png',
              },
              {
                  text: 'DC POWER AREA',
                  src: '../../img/buy-dc-power-visa.svg',
              },

          ],
          popularTopics: [
                'Here is a popular topic for you right here',
                'Here is another popular topic. Cool, right?',
                'What about this popular topic. Check it out.',
                'Last popular topic',

          ],
          recentTopics: [
              'This topic is so hot right now.',
              'Here is another recent topic that you should know about',
              'Topic - fresh off the presses',
              'Everyone is talking about this thing right now',

          ],
          latestReplies: [
              'This just in - someone replied',
              'Someone is saying something about this thing',
              'Someone else is saying something else about this other thing',
              'The very latest reply',
          ],
          footerRightItems: [
              {
                  text: 'facebook',
                  img: 'footer-facebook.png',
              },
                            {
                  text: 'twitter',
                  img: 'footer-twitter.png',
              },
                            {
                  text: 'youtube',
                  img: 'footer-youtube.png',
              },
                            {
                  text: 'pinterest',
                  img: 'footer-pinterest.png',
              },
                            {
                  text: 'periscope',
                  img: 'footer-periscope.png',
              },
          ],
      }
  }

}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

@import '../style/general.scss';

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.all_caps_title {
    @include all-caps-title;
}

.info_text {
    h6 {
        padding: 10px 0;
        margin-top: 10px;
    }
    p {
        font-size: x-small;
    }   

}

.menu_list {
    @include flex-column;

    h6 {
    padding: 10px;
    margin-top: 10px;
    }
    ul {                
        list-style-type: none;
        padding: 0;

        li {                
            display: block;
            margin: 0 10px;
            font-size: 11px;
            height: 40px;
            overflow: hidden;
            padding-bottom: 10px;
            border-bottom: 1px solid $colorSilverChalice;

            a {
                
                text-decoration: none;
                color: $colorShark;
                padding: 0;
                &:hover {                        
                    color: $colorSalmon;
                }
            }
        }
    }
}

.footer_bottom_container {
    height: 50px;
    border-top: 1px solid $colorLightGrey;

    .copyright {
        color: $colorSilverChalice;
        font-size: xx-small;
        

        a {
            color: $colorNevada;
            text-decoration: none;
            &:hover {
                color: $colorSalmon;
            }
        }
    }

    .footer-right {
        li {
            @include li-menu-horizontal;
            margin: 15px 5px;
        }
    }
}




/* scss stolen from dc comics project
* {
    text-align: left;
    color: #fff;
}

.full-footer-container {
    position: relative;
}*/

/*main footer contents */

/*.footer-container {
    @include flex-row-around;
    height: 400px;
    margin-top: 50px;


    .footer-left {
        display: flex;
        width: 40%;
        padding: 5% 0 5% 15%;


        .menu-col {

                h6 {
                padding: 10px;
                margin-top: 10px;
                }
                ul {
                list-style-type: none;
                padding: 0;

                    li {
                    display: inline-block;
                    margin: 0 10px;
                    font-size: 11px;
                    vertical-align: center;
                    padding: 0;

                        a {
                        text-decoration: none;
                        color: grey;
                        &:hover {
                            color: $colorWhite;
                        }
                        }
                    }
                }
                
        }
    }
}


.footer-right {
    width: 60%;
    @include flex-row-center;

        img {
        max-height: 400px;
        padding-left: 5%;
        }
        a {
            text-decoration: none;
        }
}    */    


/*footer bottom banner */

/*.footer-bottom-banner {
    height: 70px;
    background-color:#242424;
    display: flex;
    width: 100%;
}

.footer-bottom-banner img {
    max-height: 20px;
    &:hover {
        border: solid 1px white;
        border-radius: 50%;
    }
}

#follow {
    color: blue;
    &:hover {
        color: white;
    }
}

.footer-right li {
    @include li-menu-horizontal;
    margin: 0 5px;

}

button {
    align-self: center;
    padding: 10px;
    background-color: transparent;
    border: solid;
    border-color: blue;
    position: absolute;
    top: 15px;
    left: 15%;
    &:hover {
        border-color: white;
    }

    #button {
        text-decoration: none;
        color: white;
    }
}*/



    




</style>