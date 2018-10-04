<template>
    <div>

        <JqxComboBox :theme="'material'" ref="myComboBox" style="float: left; margin-top: 270px;"
                     :width="150" :height="25" :source="dataAdapter" :selectedIndex="0"
                     :dropDownVerticalAlignment="'top'" :dropDownWidth="200"
                     :displayMember="'ContactName'" :valueMember="'CompanyName'">
        </JqxComboBox>

        <div style="float: left; font-size: 13px; font-family: Verdana; margin-left: 100px; margin-top:270px;">
            <h3>Alignment</h3>

            <JqxRadioButton :theme="'material'" @checked="topBtnOnChecked()" :checked="true">
                Top
            </JqxRadioButton>

            <JqxRadioButton :theme="'material'" style="margin-top: 10px" @checked="bottomBtnOnChecked()">
                Bottom
            </JqxRadioButton>

        </div>
    </div>
</template>

<script>
    import JqxComboBox from "jqwidgets-scripts/jqwidgets-vue/vue_jqxcombobox.vue";
    import JqxRadioButton from "jqwidgets-scripts/jqwidgets-vue/vue_jqxradiobutton.vue";

    export default {
        components: {
            JqxComboBox,
            JqxRadioButton
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
                url: 'customers.txt',
                async: false
            };
        },
        methods: {
            bottomBtnOnChecked: function () {
                this.$refs.myComboBox.dropDownVerticalAlignment = 'bottom';
            },
            topBtnOnChecked: function () {
                this.$refs.myComboBox.dropDownVerticalAlignment = 'top';
            }
        }
    };
</script>

<style>
  
  
</style>