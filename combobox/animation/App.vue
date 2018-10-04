<template>
    <div>
        <div id='selectionlog'>
            <h3>Animation Type</h3>

            <JqxRadioButton :theme="'material'" @checked="noneAnimationOnChecked()">
                None
            </JqxRadioButton>

            <JqxRadioButton :theme="'material'" @checked="slideAnimationOnChecked()">
                Slide
            </JqxRadioButton>

            <JqxRadioButton :theme="'material'" @checked="fadeAnimationOnChecked()" :checked="true">
                Fade
            </JqxRadioButton>
        </div>

        <JqxComboBox :theme="'material'" ref="myComboBox"
                     :width="150" :height="25" :source="dataAdapter" :selectedIndex="0"
                     :animationType="'fade'" :dropDownHorizontalAlignment="'right'"
                     :displayMember="'ContactName'" :valueMember="'CompanyName'">
        </JqxComboBox>
    </div>
</template>

<script>
    import JqxRadioButton from "jqwidgets-scripts/jqwidgets-vue/vue_jqxradiobutton.vue";
    import JqxComboBox from "jqwidgets-scripts/jqwidgets-vue/vue_jqxcombobox.vue";

    export default {
        components: {
            JqxRadioButton,
            JqxComboBox
        },
        data: function () {
            return {
                dataAdapter: new jqx.dataAdapter(this.source)
            }
        },
        beforeCreate: function () {
            this.source = {
                datatype: 'json',
                datafields: [
                    { name: 'CompanyName' },
                    { name: 'ContactName' }
                ],
                id: 'id',
                url: 'customers.txt'
            };
        },
        methods: {
            noneAnimationOnChecked: function () {
                this.$refs.myComboBox.animationType = 'none';
            },
            slideAnimationOnChecked: function () {
                this.$refs.myComboBox.animationType = 'slide';
            },
            fadeAnimationOnChecked: function () {
                this.$refs.myComboBox.animationType = 'fade';
            }
        }
    };
</script>

<style>
  
    #selectionlog {
        float: left;
        font-size: 13px;
        font-family: Verdana;
    }

    .jqx-radiobutton {
        margin-top: 10px;
    }

    .jqx-combobox {
        float: left;
        margin-top: 20px;
        margin-left: 100px;
    }
  
</style>