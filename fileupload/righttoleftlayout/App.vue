<template>
    <JqxFileUpload 
                   :width="300" :uploadUrl="'upload.php'" :fileInputName="'fileToUpload'" :rtl="true">
    </JqxFileUpload>
</template>

<script>
    import JqxFileUpload from "jqwidgets-scripts/jqwidgets-vue/vue_jqxfileupload.vue";

    export default {
        components: {
            JqxFileUpload
        }
    } 
</script>

<style>
  @import 'https://www.jqwidgets.com/vue/jqwidgets/styles/jqx.base.css';
  
</style>