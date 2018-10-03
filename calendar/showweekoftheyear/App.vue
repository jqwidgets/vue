<template>
    <JqxCalendar
            :width="220" :height="220" 
            :showWeekNumbers="true"  :rowHeaderWidth="25">
    </JqxCalendar>
</template>

    <script>
    import JqxCalendar from 'jqwidgets-scripts/jqwidgets-vue/vue_jqxcalendar.vue';

    export default {
        components: {
            JqxCalendar
        }
    }
</script>

<style>   
  @import 'https://www.jqwidgets.com/vue/jqwidgets/styles/jqx.base.css';
</style>