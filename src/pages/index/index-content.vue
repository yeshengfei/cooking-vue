<template>
    <div class="cpn-wrap">
        {{contentData.name}}
    </div>
</template>
<style scoped lang="sass">
    .cpn-wrap
        display: inline-block
        min-height: 400px

</style>
<script>
    export default{
        props : ['content-data'],

        data(){
            return{

            }
        }
    }
</script>
