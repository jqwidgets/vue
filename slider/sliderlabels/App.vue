<template>
    <JqxSlider
         :width="400"  :height="60"  :min="0" :max="20"
         :value="7"  :ticksFrequency="5"  :showMinorTicks="true" 
         :showTickLabels="true"  :minorTicksFrequency="1"
    />
</template>

<script>
    import JqxSlider from "jqwidgets-scripts/jqwidgets-vue/vue_jqxslider.vue";

    export default {
        components: {
            JqxSlider
        }
    }
</script>

<style>
  @import 'https://www.jqwidgets.com/vue/jqwidgets/styles/jqx.base.css';
    .jqx-slider {
        margin-top: 50px;
    }
  
</style>