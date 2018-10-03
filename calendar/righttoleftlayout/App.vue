<template>
    <JqxCalendar
            :width="220" :height="220" 
            :rtl="true" :culture="'he-IL'">
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