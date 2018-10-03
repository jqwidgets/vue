<template>
    <JqxEditor :width="getWidth" :height="400" :lineBreak="'div'">
    </JqxEditor>
</template>

<script>
    import JqxEditor from "jqwidgets-scripts/jqwidgets-vue/vue_jqxeditor.vue";

    export default {
        components: {
            JqxEditor
        },
        data: function () {
            return {
                getWidth: '90%'
            }
        }
    }
</script>

<style>
  @import 'https://www.jqwidgets.com/vue/jqwidgets/styles/jqx.base.css';
</style>