<template>
    <div>
        <div class="content-wrap">
            <index-content :content-data="content"></index-content>
            <side-bar :list-data="list"></side-bar>
        </div>

    </div>
</template>
<style lang="sass" scoped>
    .content-wrap
        margin: 60px auto
        width: 1000px
</style>
<script>
    import IndexContent from './index-content.vue';
    import SideBar from './side-bar.vue';

    export default{
        components : {
            IndexContent,
            SideBar
        },
        data( ) {
            return {
                list: [
                    {name : 'menu1', selected : true},
                    {name : 'menu2', selected : false},
                    {name : 'menu3', selected : false},
                    {name : 'menu4', selected : false},
                    {name : 'menu5', selected : false}
                ],
                content : {}
            }
        },
        events: {
            'list-change': function (data) {
                this.content = data;
            }
        }
    }
</script>
