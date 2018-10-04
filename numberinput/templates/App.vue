<template>
    <div style="font-size: 13px; font-family: Verdana; float: left;">
        <div style="margin-top: 10px;">
            Default
        </div>
        <div style="margin-top: 3px;">
            <JqxNumberInput :theme="'material'" :spinButtons="true"
                            :width="250"
                            :height="25">
            </JqxNumberInput>
        </div>
        <div style="margin-top: 10px;">
            Primary
        </div>
        <div style="margin-top: 3px;">
            <JqxNumberInput :theme="'material'" :template="'primary'"
                            :spinButtons="true"
                            :width="250"
                            :height="25">
            </JqxNumberInput>
        </div>
        <div style="margin-top: 10px;">
            Success
        </div>
        <div style="margin-top: 3px;">
            <JqxNumberInput :theme="'material'" :template="'success'"
                            :spinButtons="true"
                            :width="250"
                            :height="25">
            </JqxNumberInput>
        </div>
        <div style="margin-top: 10px;">
            Info
        </div>
        <div style="margin-top: 3px;">
            <JqxNumberInput :theme="'material'" :template="'info'"
                            :spinButtons="true"
                            :width="250"
                            :height="25">
            </JqxNumberInput>
        </div>
        <div style="margin-top: 10px;">
            Warning
        </div>
        <div style="margin-top: 3px;">
            <JqxNumberInput :theme="'material'" :template="'warning'"
                            :spinButtons="true"
                            :width="250"
                            :height="25">
            </JqxNumberInput>
        </div>
        <div style="margin-top: 10px;">
            Danger
        </div>
        <div style="margin-top: 3px;">
            <JqxNumberInput :theme="'material'" :template="'danger'"
                            :spinButtons="true"
                            :width="250"
                            :height="25">
            </JqxNumberInput>
        </div>
    </div>
</template>
<script>
    import JqxNumberInput from "jqwidgets-scripts/jqwidgets-vue/vue_jqxnumberinput.vue";

    export default {
        components: {
            JqxNumberInput
        }
    }
</script>

<style>
  
  
</style>
