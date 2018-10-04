<template>
    <div>
        <!--Notifications-->
        <JqxNotification :theme="'material'" ref="msgNotification"
                         :width="250" :position="'top-right'" :opacity="0.9" :autoOpen="false"
                         :autoClose="true" :animationOpenDelay="800" :autoCloseDelay="3000" :template="'info'">
            <div>
                Welcome to our website.
            </div>
        </JqxNotification>
        <JqxNotification :theme="'material'" ref="timeNotification"
                         :width="250" :position="'top-right'" :opacity="0.9" :autoOpen="false"
                         :autoClose="true" :animationOpenDelay="800" :autoCloseDelay="3000" :template="'time'">
            <div>Current time: <span id="currentTime" style="font-weight: bold;"></span>.</div>
        </JqxNotification>
        <!--Layout-->
        <JqxButton :theme="'material'" :width="230" :height="22" @click="onClickOpenMessageNotification()">
            Open a message notification
        </JqxButton>
        <br /><br />
        <JqxButton :theme="'material'" :width="230" :height="22" @click="onClickOpenTimeNotification()">
            Open a current time notification
        </JqxButton>
    </div>
</template>
<script>
    import JqxNotification from "jqwidgets-scripts/jqwidgets-vue/vue_jqxnotification.vue";
    import JqxButton from "jqwidgets-scripts/jqwidgets-vue/vue_jqxbuttons.vue";

    export default {
        components: {
            JqxNotification,
            JqxButton
        },
        methods: {
            onClickOpenMessageNotification: function() {
                this.$refs.msgNotification.open();
            },
            onClickOpenTimeNotification: function () {
                let date = new Date();
                let minutes = date.getMinutes();
                let minutesString = '';
                if (minutes < 10) {
                    minutesString = "0" + minutes;
                } else {
                    minutesString = "" + minutes;
                }

                let seconds = date.getSeconds();
                let secondsString = '';
                if (seconds < 10) {
                    secondsString = "0" + seconds;
                } else {
                    secondsString = "" + seconds;
                }

                let timeSpan = document.getElementById('currentTime');
                timeSpan.innerText = date.getHours() + ":" + minutesString + ":" + secondsString;
                this.$refs.timeNotification.open();
            }
        }
    }
</script>

<style>
  
  
</style>
