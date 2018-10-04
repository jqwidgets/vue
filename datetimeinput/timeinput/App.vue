<template>
    <JqxDateTimeInput 
        :width="250" :height="25" :formatString="'T'"
        :showTimeButton="true" :showCalendarButton="false">
    </JqxDateTimeInput>
</template>

<script>
    import JqxDateTimeInput from "jqwidgets-scripts/jqwidgets-vue/vue_jqxdatetimeinput.vue";

    export default {
        components: {
            JqxDateTimeInput
        }
    };
</script>

<style>
  @import 'https://www.jqwidgets.com/vue/jqwidgets/styles/jqx.base.css';
  
</style>