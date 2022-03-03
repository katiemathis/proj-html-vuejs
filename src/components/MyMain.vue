<template>
    <div class="main-container">
        <MyJumbotron />

    </div>
</template>

<script>
import MyJumbotron from './partials/MyJumbotron.vue'

export default {
    name: 'MyMain',
    components: {
        MyJumbotron,
    },

    data () {
        return 
    

    }
}
</script>

<style scoped lang="scss">

@import '../style/general.scss';

</style>