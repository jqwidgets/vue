<template>
    <div>
        <div>The value is: {{ value }}</div><br />

        <JqxSlider :theme="'material'" v-model="value" :width="200" :height="25" />
    </div>
</template>

<script>
    import JqxSlider from 'jqwidgets-scripts/jqwidgets-vue/vue_jqxslider.vue';

    export default {
        components: {
            JqxSlider
        },
        data: function () {
            return {
                value: 5
            }
        }
    }
</script>

<style>
  
   
</style>