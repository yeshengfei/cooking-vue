<template>
    <div class="header-wrap">
        {{myMsg}}
    </div>
</template>
<style scoped>
    .header-wrap {
        color: pink;
        width: 100%;
        height: 50px;
        background: black;
        position: absolute;
        top: 0;
    }
</style>
<script>
    export default{
        data : function( ) {
            return {
                myMsg : 'this is header'
            }
        }
    }
</script>
