<template>
    <div>
        <JqxKnob :theme="'material'" ref="myKnob" @change="myKnobOnChange($event)"
                 :width="400" :height="400"
                 :value="30" :min="0" :max="100" :rotation="'clockwise'"
                 :styleProperty="{ fill: '#fff' }" :progressBar="progressBar" :pointer="pointer"
                 :dial="dial" :startAngle="270" :endAngle="630">
        </JqxKnob>

        <input ref="myInput" @change="myInputOnChange()" value="30">

    </div>
</template>
<script>
    import JqxKnob from "jqwidgets-scripts/jqwidgets-vue/vue_jqxknob.vue";
    import JqxInput from "jqwidgets-scripts/jqwidgets-vue/vue_jqxinput.vue";

    export default {
        components: {
            JqxKnob,
            JqxInput
        },
        data: function () {
            return {
                progressBar: {
                    style: { fill: '#00a644' },
                    background: { fill: '#eeeeee' },
                    size: '30%',
                    offset: '70%'
                },
                pointer: {
                    type: 'line',
                    style: { fill: '#00a644' },
                    size: '30%',
                    offset: '70%',
                    thickness: 20
                },
                dial: {
                    style: {
                        fill: '#fff'
                    },
                    innerRadius: '68%',
                    outerRadius: '92%',
                    startAngle: 0,
                    endAngle: 360
                }
            }
        },
        methods: {
            myKnobOnChange: function (event) {
                if (event.target.nodeName === 'INPUT')
                    return;
                this.$refs.myInput.value = event.args.value;
            },
            myInputOnChange: function () {
                this.$refs.myKnob.val(this.$refs.myInput.value);
            }
        }
    }
</script>

<style>
    input {
        width: 110px;
        height: 70px;
        font-weight: bold;
        font-size: 48px;
        text-align: center;
        color: #00a644;
        border: none;
        outline: none;
        position: relative;
        left: 145px;
        top: -230px;
    }
</style>
