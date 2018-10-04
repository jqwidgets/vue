<template>
    <div>
        <div>The value is: {{ value }}</div><br />

        <JqxFormattedInput v-model="value" :width="200" :height="25" :radix="'decimal'" :spinButtons="true" :dropDown="true" />
    </div>
</template>

<script>
    import JqxFormattedInput from 'jqwidgets-scripts/jqwidgets-vue/vue_jqxformattedinput.vue';

    export default {
        components: {
            JqxFormattedInput
        },
        data: function () {
            return {
                value: 20
            }
        }
    }
</script>

<style>
  @import 'https://www.jqwidgets.com/vue/jqwidgets/styles/jqx.base.css';
   
</style>