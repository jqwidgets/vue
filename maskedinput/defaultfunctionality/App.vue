<template>
    <div>
        <div id="jqxWidget" style="font-size: 13px; font-family: Verdana;">
            <div style="margin-top: 10px;">
                Numeric
            </div>
            <JqxMaskedInput :theme="'material'" ref="numericInput"
                            :width="250"
                            :height="25">
            </JqxMaskedInput>
            <div style='margin-top: 10px;'>
                Zip Code
            </div>
            <JqxMaskedInput :theme="'material'" ref="zipCodeInput"
                            :mask="'#####-####'"
                            :width="250"
                            :height="25">
            </JqxMaskedInput>
            <div style='margin-top: 10px;'>
                SSN
            </div>
            <JqxMaskedInput :theme="'material'" ref="ssnInput"
                            :mask="'###-##-####'"
                            :width="250"
                            :height="25">
            </JqxMaskedInput>
            <div style='margin-top: 10px;'>
                Phone Number
            </div>
            <JqxMaskedInput :theme="'material'" ref="phoneInput"
                            :mask="'(###)###-####'"
                            :width="250"
                            :height="25">
            </JqxMaskedInput>
            <div style='margin-top: 10px;'>
                IP Address (ex: 255.255.255.255)
            </div>
            <JqxMaskedInput :theme="'material'" ref="regexInput"
                            :mask="'[0-2][0-5][0-5].[0-2][0-5][0-5].[0-2][0-5][0-5].[0-2][0-5][0-5]'"
                            :width="250"
                            :height="25">
            </JqxMaskedInput>
            <div style='margin-top: 10px;'>
                Disabled
            </div>
            <JqxMaskedInput :theme="'material'" ref="disabledInput"
                            :disabled="true"
                            :width="250"
                            :height="25">
            </JqxMaskedInput>
        </div>
        <br />
        <JqxButton :theme="'material'" @click="clear()" :width="120">Clear Values</JqxButton>
    </div>
</template>
<script>
    import JqxMaskedInput from "jqwidgets-scripts/jqwidgets-vue/vue_jqxmaskedinput.vue";
    import JqxButton from "jqwidgets-scripts/jqwidgets-vue/vue_jqxbuttons.vue";

    export default {
        components: {
            JqxMaskedInput,
            JqxButton
        },
        methods: {
            clear: function() {
                this.$refs.numericInput.clear();
                this.$refs.zipCodeInput.clear();
                this.$refs.ssnInput.clear();
                this.$refs.phoneInput.clear();
                this.$refs.regexInput.clear();
                this.$refs.disabledInput.clear();
            }
        }
    }
</script>

<style>
  
   
</style>