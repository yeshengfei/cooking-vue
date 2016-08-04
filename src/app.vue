<template>
  <header-cpn></header-cpn>
  <div class="content-wrap">
      <index-content :content-data="content"></index-content>
      <side-bar :list-data="list"></side-bar>
  </div>
  <footer-cpn></footer-cpn>
</template>

<script>
  import HeaderCpn from './components/common/header.vue';
  import FooterCpn from './components/common/footer.vue';
  import SideBar from './pages/index/side-bar.vue';
  import IndexContent from './pages/index/index-content.vue';

  export default {
    name: 'app',
    components: {
        HeaderCpn,
        FooterCpn,
        SideBar,
        IndexContent
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
  };
</script>

<style lang="sass" scoped>
  .content-wrap
    margin: 60px auto
    width: 1000px
</style>