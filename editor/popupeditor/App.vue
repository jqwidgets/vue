<template>
    <div>
        <JqxButton :theme="'material'" @click="btnOnClick()" :width="120">Open Editor</JqxButton>

        <JqxWindow :theme="'material'" ref="myWindow"
                   :width="600" :height="400" :maxWidth="800"
                   :autoOpen="false" :resizable="false" :position="'top, left'">
            <div>jqxEditor</div>
            <JqxEditor ref="myEditor" :auto-create="false" />
        </JqxWindow>
    </div>
</template>

<script>
    import JqxEditor from "jqwidgets-scripts/jqwidgets-vue/vue_jqxeditor.vue";
    import JqxWindow from "jqwidgets-scripts/jqwidgets-vue/vue_jqxwindow.vue";
    import JqxButton from "jqwidgets-scripts/jqwidgets-vue/vue_jqxbuttons.vue";

    export default {
        components: {
            JqxEditor,
            JqxWindow,
            JqxButton
        },
        methods: {
            btnOnClick: function () {
                const editorOptions = {
                    theme: 'material',
                    width: '100%',
                    height: '92%',
                    tools: 'bold | italic | underline | font | size'
                }

                this.$refs.myEditor.createComponent(editorOptions);

                this.$refs.myWindow.open();
            }
        }
    }
</script>

<style>
</style>