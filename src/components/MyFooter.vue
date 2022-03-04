<template>
    <div class="footer_container">
        <div class="col-8 m-auto">
            <div class="row footer_lists">
                <div class="col info_text">
                    <h6 class="all_caps_footer">avada tech forum</h6>
                    <p class="footer_text_block">Lorem, ipsum dolor sit amet consectetur adipisicing elit. 
                        Cumque, illo iste optio atque molestias distinctio, 
                        enim modi tempora asperiores rem voluptate, blanditiis iure! 
                        Ullam fuga earum libero voluptas, dicta excepturi.</p>
                </div>
                <div class="col menu_list">
                    <h6 class="all_caps_footer">Popular Topics</h6>
                    <ul class="menu-col" v-for="(popularTopic, a) in popularTopics" :key="a">
                        <li><span class="list_decoration"><i class="fa-solid fa-angle-right"></i></span><a href="#" target="_blank" rel="noopener">{{popularTopic}}</a></li>
                        <!--<li class="hide"><a href="#" target="_blank" rel="noopener">Here is some hidden text. You can only see it if you click on the menu item.</a></li>-->
                    </ul>
                </div>
                <div class="col menu_list">
                    <h6 class="all_caps_footer">Recent Topics</h6>
                    <ul class="menu-col" v-for="(recentTopic, a) in recentTopics" :key="a">
                        <li><span class="list_decoration"><i class="fa-solid fa-angle-right"></i></span><a href="#" target="_blank" rel="noopener">{{recentTopic}}</a></li>
                    </ul>
                </div>
                <div class="col menu_list">
                    <h6 class="all_caps_footer">Latest Replies</h6>
                    <ul class="menu-col" v-for="(latestReply, a) in latestReplies" :key="a">
                        <li><span class="list_decoration"><i class="fa-solid fa-angle-right"></i></span><a href="#" target="_blank" rel="noopener">{{latestReply}}</a></li>
                    </ul>
                </div>

            </div>
        </div>
        <div class="footer_bottom_container">
            <div class="col-8 m-auto">
                <div class="row footer_bottom">
                    <div class="col-9 m-auto">
                        <p class="copyright"><span><i class="fa-regular fa-copyright copyright_icon"></i></span> Copyright 2012 - 2020 | Avada Theme by <a href="#">Theme Fusion</a> | All Rights Reserved | Powered by <a href="https://www.linkedin.com/in/katiepalumbo/">Katie</a></p>
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

</template>

<script>

export default {
    name: 'MyFooter',
    props: {
        'popularTopics': Array,
        'recentTopics': Array,
        'latestReplies': Array,
    },
    data () {
      return {
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

/*.hide {
    display: none;
}*/

.all_caps_footer {
    @include all-caps-footer;
}

.info_text {
    h6 {
        padding: 10px 0;
        margin-top: 10px;
    }
    p {
        font-size: x-small;
        color: $colorSilverChalice;
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
            min-height: 20px;
            //overflow: hidden;
            padding-bottom: 5px;
            border-bottom: 1px solid $colorLightGrey;
            &:hover {
                border-bottom: 1px solid $colorSilverChalice;
            }


            .list_decoration {
                width: 10px;
                min-height: 20px;
                margin-right: 2px;
                float: left;
                font-size: 0.8em;
                font-weight: 400;
            }


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

        .copyright_icon {
            padding-bottom: 2px;
        }

        

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