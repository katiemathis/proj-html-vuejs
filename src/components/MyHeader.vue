<template>
<!-- all'interno di header ho il logo (left) e menu di navigazione (right) 
che viene popolato in modo dinamico dalle props passato da app.vue -->
<div class="header-container">
    <div class="col-8 m-auto">
        <div class="row">
            <!-- logo -->
            <div class="col-3 logo_container">
                <div class="logo_row">
                    <img class="logo" alt="Avada logo" src="../assets/images/logo-2x.png">
                </div>
            </div>
            <!-- menu di navigazione dinamico -- i dati si trovano in app.vue -->
            <div class="col-6">
                <div class="menu">
                    <ul v-for="(navMenuItem, index) in navMenuItems" :key="index">
                        <li>
                            <a href="#" target="_blank" rel="noopener">{{navMenuItem}}</a>
                            <div class="active"></div>
                        </li>
                    </ul>
                </div>
            </div>
            <!-- button -->
            <div class="col-2">
                <div class="button">
                    <button class="btn_header">
                        JOIN US
                    </button>
                </div>
            </div>
            <!-- search icon -->
            <div class="col-1 justify-content-center align-items-center m-auto">
                <div class="row search_icon m-auto">
                    <i class="fa-solid fa-magnifying-glass"></i>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
//sotto vedo le props passate da app.vue che uso per il nav
export default {
    name: 'MyHeader',
    props: {
        'navMenuItems': Array,
    }

}
</script>

<style scoped lang="scss">

@import '../style/general.scss';

//tutte le regole css
.header-container {
    height: 70px;
    background-color: $colorEasternBlue;

    //regole logo

    .logo_container {

        .logo_row {
            max-height: 70px;

            .logo {
                //margin-top: 20px;
                max-height: 40px;
                margin-top:15px;
                object-fit: cover;
                &:hover {
                    cursor: pointer;
                }

            }
        }

    }


    //regole nav

    .menu {
    @include flex-row-around;
    margin-top: 10px;

    
        ul {
            list-style-type: none;
            padding: 0;
            margin: 1em 0 0 0;

            li {
                @include li-menu-horizontal;
                height: 70px;
                &:hover {
                    cursor: pointer;
                    a {
                        color: $colorSalmon;
                    }
                    .active {
                        display: block;
                    }
                }

                a{
                    color: $colorWhite;
                    text-decoration: none;
                }
                .active {
                    width: 0;
                    height: 0;
                    border: 15px solid transparent;
                    border-bottom: 0;
                    border-top: 20px solid $colorEasternBlue;
                    display: none;
                    position: absolute;
                    top: 60px;
                }

                
            }
            
        }
    }

    //regole button

    .btn_header {
        @include all_caps_button;
        background-color: $colorShark;
        color: $colorWhite;
        margin-top: 25px;
        padding: 5px 30px;
        &:hover {
            color: $colorSalmon;
        }

    }

    //regole search icon

    .fa-magnifying-glass {
        color: $colorWhite;
        transform: translateY(-60%);
        &:hover {
            cursor: pointer;
            color: $colorSalmon;
        }
    }
}

</style>