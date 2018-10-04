<template>
    <div style="height: 300px;">
        <JqxMenu :mode="'vertical'"
                 :width="150"
                 :height="225">
            <ul>
                <li>
                    <img style="float: left; margin-right: 5px;" src="https://www.jqwidgets.com/vue/images/mailIcon.png" /><span>Mail</span>
                </li>
                <li>
                    <img style="float: left; margin-right: 5px;" src="https://www.jqwidgets.com/vue/images/calendarIcon.png" /><span>Calendar</span>
                </li>
                <li>
                    <img style="float: left; margin-right: 5px;" src="https://www.jqwidgets.com/vue/images/contactsIcon.png" /><span>Contacts</span>
                </li>
                <li>
                    <img style="float: left; margin-right: 5px;" src="https://www.jqwidgets.com/vue/images/folder.png" /><span>
                        <span>Inbox</span>
                    </span>
                    <ul>
                        <li>
                            <img style="float: left; margin-right: 5px;" src="https://www.jqwidgets.com/vue/images/folder.png" /><span>jQWidgets</span>
                            <ul>
                                <li>
                                    <img style="float: left; margin-right: 5px;" src="https://www.jqwidgets.com/vue/images/folder.png" /><span>Admin</span>
                                </li>
                                <li>
                                    <img style="float: left; margin-right: 5px;" src="https://www.jqwidgets.com/vue/images/folder.png" /><span>Corporate</span>
                                </li>
                                <li>
                                    <img style="float: left; margin-right: 5px;" src="https://www.jqwidgets.com/vue/images/folder.png" /><span>Finance</span>
                                </li>
                                <li>
                                    <img style="float: left; margin-right: 5px;" src="https://www.jqwidgets.com/vue/images/folder.png" /><span>Other</span>
                                </li>
                            </ul>
                        </li>
                        <li>
                            <img style="float: left; margin-right: 5px;" src="https://www.jqwidgets.com/vue/images/folder.png" /><span>Personal</span>
                        </li>
                    </ul>
                </li>
                <li>
                    <img style="float: left; margin-right: 5px;" src="https://www.jqwidgets.com/vue/images/recycle.png" />
                    <span>Deleted Items</span>
                    <ul>
                        <li>
                            <img style="float: left; margin-right: 5px;" src="https://www.jqwidgets.com/vue/images/folder.png" /><span>Today</span>
                        </li>
                        <li>
                            <img style="float: left; margin-right: 5px;" src="https://www.jqwidgets.com/vue/images/folder.png" /><span>
                                Last
                                Week
                            </span>
                        </li>
                        <li>
                            <img style="float: left; margin-right: 5px;" src="https://www.jqwidgets.com/vue/images/folder.png" /><span>
                                Last
                                Month
                            </span>
                        </li>
                    </ul>
                </li>
                <li>
                    <img style="float: left; margin-right: 5px;" src="https://www.jqwidgets.com/vue/images/settings.png" /><span>Settings</span>
                    <ul style="width: 230px;">
                        <li>
                            <JqxCheckBox style="float: left; margin-right: 5px;" :checked="true">
                            </JqxCheckBox>
                            Enable Auto-Save
                        </li>
                        <li>
                            <JqxCheckBox style="float: left; margin-right: 5px;">
                            </JqxCheckBox>
                            Send email as anonymous
                        </li>
                        <li>
                            <JqxCheckBox style="float: left; margin-right: 5px;">
                            </JqxCheckBox>
                            Save sent emails
                        </li>
                    </ul>
                </li>
                <li>
                    <img style="float: left; margin-right: 5px;" src="https://www.jqwidgets.com/vue/images/notesIcon.png" /><span>Notes</span>
                </li>
                <li>
                    <img style="float: left; margin-right: 5px;" src="https://www.jqwidgets.com/vue/images/favorites.png" /><span>Favorites</span>
                </li>
            </ul>
        </JqxMenu>
    </div>
</template>
<script>
    import JqxMenu from "jqwidgets-scripts/jqwidgets-vue/vue_jqxmenu.vue";
    import JqxCheckBox from "jqwidgets-scripts/jqwidgets-vue/vue_jqxcheckbox.vue";

    export default {
        components: {
            JqxMenu,
            JqxCheckBox
        }
    }
</script>

<style>
  @import 'https://www.jqwidgets.com/vue/jqwidgets/styles/jqx.base.css';
</style>
