<template>
    <div style="float: left;">
        <JqxMenu :source="source"
                 :mode="'vertical'"
                 :width="180"
                 :height="180">
        </JqxMenu>
    </div>
</template>
<script>
    import JqxMenu from "jqwidgets-scripts/jqwidgets-vue/vue_jqxmenu.vue"

    export default {
        components: {
            JqxMenu
        },
        data: function () {
            return {
                source: [
                    {
                        html: "<img src='https://www.jqwidgets.com/vue/images/mailIcon.png'/><span style='position: relative; left: 3px; top: -2px;'>Mail</span>",
                        items: [
                            { html: "<img src='https://www.jqwidgets.com/vue/images/calendarIcon.png'/><span style='position: relative; left: 3px; top: -2px;'>Calendar</span>" },
                            { html: "<img src='https://www.jqwidgets.com/vue/images/contactsIcon.png'/><span style='position: relative; left: 3px; top: -2px;'>Contacts</span>" }
                        ]
                    },
                    {
                        html: "<img src='https://www.jqwidgets.com/vue/images/folder.png'/><span style='position: relative; left: 3px; top: -2px;'>Inbox</span>",
                        items: [
                            { html: "<img src='https://www.jqwidgets.com/vue/images/folder.png'/><span style='position: relative; left: 3px; top: -2px;'>Admin</span>" },
                            { html: "<img src='https://www.jqwidgets.com/vue/images/folder.png'/><span style='position: relative; left: 3px; top: -2px;'>Corporate</span>" },
                            { html: "<img src='https://www.jqwidgets.com/vue/images/folder.png'/><span style='position: relative; left: 3px; top: -2px;'>Finance</span>" },
                            { html: "<img src='https://www.jqwidgets.com/vue/images/folder.png'/><span style='position: relative; left: 3px; top: -2px;'>Other</span>" }]
                    },
                    { html: "<img src='https://www.jqwidgets.com/vue/images/recycle.png'/><span style='position: relative; left: 3px; top: -2px;'>Deleted Items</span>" },
                    { html: "<img src='https://www.jqwidgets.com/vue/images/notesIcon.png'/><span style='position: relative; left: 3px; top: -2px;'>Notes</span>" },
                    { html: "<img src='https://www.jqwidgets.com/vue/images/settings.png'/><span style='position: relative; left: 3px; top: -2px;'>Settings</span>" },
                    { html: "<img src='https://www.jqwidgets.com/vue/images/favorites.png'/><span style='position: relative; left: 3px; top: -2px;'>Favorites</span>" }
                ]
            }
        }
    }
</script>

<style>
  @import 'https://www.jqwidgets.com/vue/jqwidgets/styles/jqx.base.css';
  
</style>
