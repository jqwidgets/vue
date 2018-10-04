<template>
    <div style="font-size: 13px; font-family: Verdana; float: left;">
        <div style='margin-top: 10px;'>
            Numeric
        </div>
        <JqxMaskedInput :theme="'material'" :rtl="true"
                        :width="250"
                        :height="25">
        </JqxMaskedInput>
        <div style='margin-top: 10px;'>
            Zip Code
        </div>
        <JqxMaskedInput :theme="'material'" :mask="'#####-####'"
                        :rtl="true"
                        :width="250"
                        :height="25">
        </JqxMaskedInput>
        <div style='margin-top: 10px;'>
            SSN
        </div>
        <JqxMaskedInput :theme="'material'" :mask="'###-##-####'"
                        :rtl="true"
                        :width="250"
                        :height="25">
        </JqxMaskedInput>
        <div style='margin-top: 10px;'>
            Date
        </div>
        <JqxMaskedInput :theme="'material'" :mask="'##/##/####'"
                        :rtl="true"
                        :width="250"
                        :height="25">
        </JqxMaskedInput>
    </div>
</template>
<script>
    import JqxMaskedInput from "jqwidgets-scripts/jqwidgets-vue/vue_jqxmaskedinput.vue";

    export default {
        components: {
            JqxMaskedInput
        }
    }
</script>

<style>
  
  
</style>
