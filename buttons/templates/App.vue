<template>
  <div>
    <JqxButton :theme="'material'" :width="80" style="float: left">Default</JqxButton>
    <JqxButton :theme="'material'" :template="'primary'" :width="80" style="float: left; margin-left: 4px">Primary</JqxButton>
    <JqxButton :theme="'material'" :template="'info'"    :width="80" style="float: left; margin-left: 4px">Info</JqxButton>
    <JqxButton :theme="'material'" :template="'success'" :width="80" style="float: left; margin-left: 4px">Success</JqxButton>
    <JqxButton :theme="'material'" :template="'warning'" :width="80" style="float: left; margin-left: 4px">Warning</JqxButton>
    <JqxButton :theme="'material'" :template="'danger'"  :width="80" style="float: left; margin-left: 4px">Danger</JqxButton>
    <JqxButton :theme="'material'" :template="'inverse'" :width="80" style="float: left; margin-left: 4px">Inverse</JqxButton>
    <JqxButton :theme="'material'" :template="'link'"    :width="80" style="float: left">Link</JqxButton>
  </div>
</template>

    <script>
    import JqxButton from 'jqwidgets-scripts/jqwidgets-vue/vue_jqxbuttons.vue';

    export default {
        components: {
            JqxButton
        }
    }
</script>

<style>
     
  
</style>