<template>
  <div>
    <b>Checkbox</b>
    <JqxCheckBox :theme="'material'" style="margin-top: 10px" :width="'30%'">eLearning</JqxCheckBox>
    <JqxCheckBox :theme="'material'" style="margin-top: 5px; margin-bottom: 10px" :width="'30%'">Mobile</JqxCheckBox>

    <b>Radio Button</b>
    <JqxRadioButton :theme="'material'" style="margin-top: 10px" :width="'30%'">On</JqxRadioButton>
    <JqxRadioButton :theme="'material'" style="margin-top: 5px; margin-bottom: 10px" :width="'30%'">Off</JqxRadioButton>

    <b>DropDown Button</b>
    <JqxDropDownButton :theme="'material'" ref="myDropDownButton" style="margin-top: 10px; margin-bottom: 10px" :width="'50%'" :height="25">
      <div>
        <ul>
          <li>Education</li>
          <li>Financial services</li>
          <li>Government</li>
          <li>Manufacturing</li>
          <li>
            Solutions
            <ul>
              <li>eLearning</li>
              <li>Mobile</li>
              <li>RIA</li>
              <li>Training</li>
            </ul>
          </li>
        </ul>
      </div>
    </JqxDropDownButton>

    <b>Switch Button</b>
    <JqxSwitchButton :theme="'material'" style="margin-top: 10px" :width="'20%'"></JqxSwitchButton>
  </div>
</template>

    <script>
    import JqxCheckBox from 'jqwidgets-scripts/jqwidgets-vue/vue_jqxcheckbox.vue';
    import JqxRadioButton from 'jqwidgets-scripts/jqwidgets-vue/vue_jqxradiobutton.vue';
    import JqxDropDownButton from 'jqwidgets-scripts/jqwidgets-vue/vue_jqxdropdownbutton.vue';
    import JqxSwitchButton from 'jqwidgets-scripts/jqwidgets-vue/vue_jqxswitchbutton.vue';

    export default {
        components: {
            JqxCheckBox,
            JqxRadioButton,
            JqxDropDownButton,
            JqxSwitchButton
        },
        mounted: function() {
            let dropDownContent = '<div style="position: relative; margin-left: 3px; margin-top: 5px;">DropDownButton</div>';
            this.$refs.myDropDownButton.setContent(dropDownContent);
        }
    }
</script>

<style>
     
  
</style>