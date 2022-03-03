<template>
    <div class="forum-sections-container">
        <div class="col-8 m-auto sections_grid m-5">
            <div class="row">
                <div class="col section_card">
                    <div>
                        icon
                    </div>
                    <div>
                        title
                    </div>
                </div>
                <div class="col section_card">
                    <div>
                        icon
                    </div>
                    <div>
                        title
                    </div>
                </div>
                <div class="col section_card">
                    <div>
                        icon
                    </div>
                    <div>
                        title
                    </div>
                </div>
                <div class="col section_card">
                    <div>
                        icon
                    </div>
                    <div>
                        title
                    </div>
                </div>
            </div>
            <div class="row">
                <div class="col section_card">
                    <div>
                        icon
                    </div>
                    <div>
                        title
                    </div>
                </div>
                <div class="col section_card">
                    <div>
                        icon
                    </div>
                    <div>
                        title
                    </div>
                </div>
                <div class="col section_card">
                    <div>
                        icon
                    </div>
                    <div>
                        title
                    </div>
                </div>
                <div class="col section_card">
                    <div>
                        icon
                    </div>
                    <div>
                        title
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
            forumSections: [
            {
                name: 'cat',
                prefix: 'fa-',
                type: 'animal',
                family: 'fas',
                color: 'orange'
            },
            {
                name: 'crow',
                prefix: 'fa-',
                type: 'animal',
                family: 'fas',
                color: 'orange'
            },
            {
                name: 'dog',
                prefix: 'fa-',
                type: 'animal',
                family: 'fas',
                color: 'orange'
            },
            {
                name: 'dove',
                prefix: 'fa-',
                type: 'animal',
                family: 'fas',
                color: 'orange'
            },
            {
                name: 'dragon',
                prefix: 'fa-',
                type: 'animal',
                family: 'fas',
                color: 'orange'
            },
            {
                name: 'horse',
                prefix: 'fa-',
                type: 'animal',
                family: 'fas',
                color: 'orange'
            },
            {
                name: 'hippo',
                prefix: 'fa-',
                type: 'animal',
                family: 'fas',
                color: 'orange'
            },
            {
                name: 'fish',
                prefix: 'fa-',
                type: 'animal',
                family: 'fas',
                color: 'orange'
            },
            
        ]
        }
    }

}
</script>

<style scoped lang="scss">

@import '../../style/general.scss';

.forum-sections-container {
    background-color: $colorLightGrey;
    padding: 20px 0 50px 0;

    .section_card{
        border: solid 1px #000;
        width: 100px;
        height: 100px;
    }
}

</style>