<template>
<div class="header-container">
    <div class="col-8 m-auto">
        <div class="row">
            <div class="col-3 logo_container">
                <div class="logo">
                    <img alt="Vue logo" src="../assets/images/logo.png">
                </div>
            </div>
            <div class="col-6">
                <div class="menu">
                    <ul v-for="(navMenuItem, index) in navMenuItems" :key="index">
                        <li><a href="#" target="_blank" rel="noopener">{{navMenuItem}}</a></li>
                    </ul>
                </div>
            </div>
            <div class="col-2">
                <div class="button">
                    <button class="btn btn_header">
                        JOIN US
                    </button>
                </div>
            </div>
            <div class="col-1">
                <div class="search_icon">
                    SEARCH ICON HERE
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: 'MyHeader',

    data () {
    return {
        navMenuItems: ['Home', 'Apple', 
        'Microsoft', 'Android', 'Forums', 'Contact Us', 
        ]
    }
        

  }

}
</script>

<style scoped lang="scss">

@import '../style/general.scss';

.header-container {
    height: 70px;
    background-color: $colorEasternBlue;

    .logo_container {

        .logo {
            margin-top: 20px;

        }

    }



    .menu {
    @include flex-row-around;
    margin-top: 10px;

    
        ul {
            list-style-type: none;
            padding: 0;
            margin: 1em 0 0 0;

            li {
                @include li-menu-horizontal;
                a {
                    color: $colorWhite;
                    text-decoration: none;

                    
              }
            }
            
        }
    }

    .btn_header {
        background-color: $colorShark;
        color: $colorWhite;
        margin-top: 20px;

    }
}

</style>