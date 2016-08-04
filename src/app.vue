<template>
    <div id="app">
        <header-cpn></header-cpn>
        <router-view></router-view>
        <footer-cpn></footer-cpn>
    </div>
  <!--<div class="content-wrap">-->
      <!--<index-content :content-data="content"></index-content>-->
      <!--<side-bar :list-data="list"></side-bar>-->
  <!--</div>-->

</template>

<script>
    import HeaderCpn from './components/common/header.vue';
    import FooterCpn from './components/common/footer.vue';



  export default {
    components: {
        HeaderCpn,
        FooterCpn
    }

  };
</script>

<style lang="sass" scoped>
  .content-wrap
    margin: 60px auto
    width: 1000px
</style>