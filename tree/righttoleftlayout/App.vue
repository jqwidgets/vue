<template>
    <JqxTree
        :width="250" :height="350" :source="source" :rtl="true">
    </JqxTree>
</template>

<script>
    import JqxTree from 'jqwidgets-scripts/jqwidgets-vue/vue_jqxtree.vue';

    export default {
        components: {
            JqxTree
        },
        data: function () {
            return {
                source:
                [
                    {
                        icon: 'https://www.jqwidgets.com/vue/images/mailIcon.png', label: 'Mail', expanded: true,
                        items:
                        [
                            { icon: 'https://www.jqwidgets.com/vue/images/calendarIcon.png', label: 'Calendar' },
                            { icon: 'https://www.jqwidgets.com/vue/images/contactsIcon.png', label: 'Contacts', selected: true }
                        ]
                    },
                    {
                        icon: 'https://www.jqwidgets.com/vue/images/folder.png', label: 'Inbox', expanded: true,
                        items:
                        [
                            { icon: 'https://www.jqwidgets.com/vue/images/folder.png', label: 'Admin' },
                            { icon: 'https://www.jqwidgets.com/vue/images/folder.png', label: 'Corporate' },
                            { icon: 'https://www.jqwidgets.com/vue/images/folder.png', label: 'Finance' },
                            { icon: 'https://www.jqwidgets.com/vue/images/folder.png', label: 'Other' },
                        ]
                    },
                    { icon: 'https://www.jqwidgets.com/vue/images/recycle.png', label: 'Deleted Items' },
                    { icon: 'https://www.jqwidgets.com/vue/images/notesIcon.png', label: 'Notes' },
                    { icon: 'https://www.jqwidgets.com/vue/images/settings.png', label: 'Settings', iconsize: 14 },
                    { icon: 'https://www.jqwidgets.com/vue/images/favorites.png', label: 'Favorites' },
                ]
            }
        }
    }
</script>

<style>
  @import 'https://www.jqwidgets.com/vue/jqwidgets/styles/jqx.base.css';
   
</style>