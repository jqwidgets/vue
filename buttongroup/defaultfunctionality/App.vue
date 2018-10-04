<template>
    <div>
        <JqxButton :theme="'material'"Group ref="myButtonGroup" @buttonclick="groupOnBtnClick($event)">
            <button style="padding: 4px 16px" id='Left' value='Left'></button>
            <button style="padding: 4px 16px" id='Center' value='Center'></button>
            <button style="padding: 4px 16px" id='Right' value='Right'></button>
        </JqxButtonGroup>

        <div style="margin-top: 10px">
            <h4>Modes</h4>
            <JqxRadioButton :theme="'material'" @checked="myDefaultModeButtonChecked()" :checked="true">Default</JqxRadioButton>
            <JqxRadioButton :theme="'material'" @checked="myRadioModeButtonChecked()">RadioButtons</JqxRadioButton>
            <JqxRadioButton :theme="'material'" @checked="myCheckBoxModeButtonChecked()">CheckBoxes</JqxRadioButton>
        </div>

        <div ref="myLog" style="margin-top: 10px;"></div>
    </div>
</template>

<script>

    import JqxButtonGroup from 'jqwidgets-scripts/jqwidgets-vue/vue_jqxbuttongroup.vue';
    import JqxRadioButton from 'jqwidgets-scripts/jqwidgets-vue/vue_jqxradiobutton.vue';

    export default {
        components: {
            JqxButtonGroup,
            JqxRadioButton
        },
        methods: {

            myDefaultModeButtonChecked: function () {
                this.$refs.myButtonGroup.mode = 'default';
            },
            myRadioModeButtonChecked: function () {
                this.$refs.myButtonGroup.mode = 'radio';
            },
            myCheckBoxModeButtonChecked: function () {
                this.$refs.myButtonGroup.mode = 'checkbox';
            },
            groupOnBtnClick: function (event) {
                let clickedButton = event.args.button;
                this.$refs.myLog.innerHTML = `Clicked: ${clickedButton[0].id}`;
            }
        }
    }
</script>

<style>
  
  
</style>