<template>
    <div>
        <JqxLoader :theme="'material'" ref="jqxLoader"
                   :text="''"
                   :width="100"
                   :height="60">
        </JqxLoader>
        <JqxButton :theme="'material'" @click="openLoaderClick($event)"
                   :width="150">
            Open Loader
        </JqxButton>
        <JqxButton :theme="'material'" @click="closeLoaderClick($event)"
                   :width="100">
            Close
        </JqxButton>
    </div>
</template>
<script>
    import JqxLoader from "jqwidgets-scripts/jqwidgets-vue/vue_jqxloader.vue";
    import JqxButton from "jqwidgets-scripts/jqwidgets-vue/vue_jqxbuttons.vue";

    export default {
        components: {
            JqxLoader,
            JqxButton
        },
        methods: {
            openLoaderClick: function (event) {
                this.$refs.jqxLoader.open();
            },
            closeLoaderClick: function (event) {
                this.$refs.jqxLoader.close();
            }
        }
    }
</script>

<style>
  
    .jqx-button {
        display: inline-block;
        margin-right: 5px;
    }
  
</style>
