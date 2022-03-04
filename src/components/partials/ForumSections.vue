<template>
    <div class="forum-sections-container">
        <div class="col-8 m-auto sections_grid m-5">
            <div class="row row-cols-4 icon-row g-4">
                <div class="col section_card" v-for="(section, index) in forumSections" :key="index">
                    <div class="icon">
                        <i :class= "`${section.prefix}${section.type} ${section.prefix}${section.family}`" 
                        class="icon_image"></i>
                        <p class="title">{{section.name}}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ForumSections',
    data() {
        return{
            content: '',
            forumSections: [
            {
                //<i class="fa-solid fa-file-lines"></i>
                name: 'News and Community',
                prefix: 'fa-',
                type: 'file-lines',
                family: 'solid',
                color: 'orange'
            },
            {
                //<i class="fa-brands fa-apple"></i>
                name: 'Apple Forum',
                prefix: 'fa-',
                type: 'apple',
                family: 'brands',
                color: 'orange'
            },
            {
                //<i class="fa-brands fa-windows"></i>
                name: 'Microsoft Forum',
                prefix: 'fa-',
                type: 'windows',
                family: 'brands',
                color: 'orange'
            },
            {
                //<i class="fa-brands fa-android"></i>
                name: 'Android Forum',
                prefix: 'fa-',
                type: 'android',
                family: 'brands',
                color: 'orange'
            },
            {
                //<i class="fa-solid fa-mug-saucer"></i>
                name: 'General Discussion',
                prefix: 'fa-',
                type: 'mug-saucer',
                family: 'solid',
                color: 'orange'
            },
            {
                //<i class="fa-solid fa-cubes"></i>
                name: 'Apps and Software',
                prefix: 'fa-',
                type: 'cubes',
                family: 'solid',
                color: 'orange'
            },
            {
                //<i class="fa-solid fa-laptop"></i>
                name: 'Gadgets and Stuff',
                prefix: 'fa-',
                type: 'laptop',
                family: 'solid',
                color: 'orange'
            },
            {
                //<i class="fa-solid fa-wrench"></i>
                name: 'Tutorials and Guides',
                prefix: 'fa-',
                type: 'wrench',
                family: 'solid',
                color: 'orange'
            },
            
        ]
        }
    },
   
}
</script>

<style scoped lang="scss">

@import '../../style/general.scss';

.forum-sections-container {
    background-color: $colorLightGrey;
    padding: 20px 0 50px 0;

    .section_card{
        justify-content: center;
        padding: 0 10px;

        .icon {
            border-top: solid 2px $colorEasternBlue;
            width: 150px;
            height: 150px;
            align-self: center;
            margin: auto;
            justify-content: center;
            align-items: center;
            text-align: center;
            background-color: $colorWhite;
            &:hover {
                cursor: pointer;
                border-top: solid 2px $colorSalmon;
            }

            .icon_image {
                margin-top: 30px;
                height: 20px;
                width: 20px;
                border-radius: 50%;
                padding: 10%;
                color: white;
                background-color: $colorSalmon;
                //font-size: 3em;
                
            }
            
            .title {
                padding: 20px 5px;
                font-size: small;
                font-weight: 600;

            }

        }
    }
}

</style>