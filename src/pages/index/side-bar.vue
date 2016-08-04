<template>
    <div class="side-bar-wrap">
        <ul>
            <li v-for="(index, value) in listData"
                @click="onListSelect(value)"
                class="{{value.selected ? 'selected' : ''}}">
                {{index}} - {{value.name}}
            </li>
            <!--<div v-for="value in cpnData">{{value}}</div>-->
        </ul>
    </div>
</template>
<style scoped lang="sass">
    .side-bar-wrap
        width: 200px
        float: left

    li.selected
        color : red

</style>
<script>
    export default{
        props : ['list-data'],

        methods : {
            onListSelect : function(value) {
                for(var key in this.listData) {
                    this.listData[key].selected = false;
                }
                value.selected = true;

                this.$dispatch('list-change', value);
            }
        }
    }
</script>
