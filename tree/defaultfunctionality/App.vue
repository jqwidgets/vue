<template>
    <div>
        <JqxExpander 
            :width="300" :height="370" :showArrow="false" :toggleMode="'none'">
            <div>Folders</div>
            <div style="overflow: hidden;">
                <JqxTree ref="myTree"
                    :width="'100%'" :height="'100%'" :source="treeSource">
                </JqxTree>
            </div>
        </JqxExpander>
    </div>
</template>

<script>
    import JqxTree from 'jqwidgets-scripts/jqwidgets-vue/vue_jqxtree.vue';
    import JqxExpander from 'jqwidgets-scripts/jqwidgets-vue/vue_jqxexpander.vue';

    export default {
        components: {
            JqxTree,
            JqxExpander
        },
        data: function () {
            return {
                treeSource:
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
                    { icon: 'https://www.jqwidgets.com/vue/images/favorites.png', label: 'Favorites' }
                ]
            }
        },
        mounted: function () {
            this.$refs.myTree.selectItem(null);
        }
    }
</script>

<style>
  @import 'https://www.jqwidgets.com/vue/jqwidgets/styles/jqx.base.css'; 
</style>