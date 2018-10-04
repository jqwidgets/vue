<template>
    <div>
        <JqxTree :theme="'material'" style="float: left;" ref="myTree"
                 @select="select($event)" @expand="expand($event)" @collapse="collapse($event)"
                 :width="250" :source="source">
        </JqxTree>

        <div style="margin-left: 20px; float: left;">
            <div>
                <span>Events:</span>

                <JqxPanel :theme="'material'" ref="myPanel" :width="250" :height="200"></JqxPanel>
            </div>
        </div>
    </div>
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
        },
        methods: {
            select: function (event) {
                this.buildElement(event, 'Selected: ');
            },
            expand: function (event) {
                this.buildElement(event, 'Expanded: ');
            },
            collapse: function (event) {
                this.buildElement(event, 'Collapsed: ');
            },
            buildElement: function (event, text) {
                const item = this.$refs.myTree.getItem(event.args.element);
                const el = document.createElement('div');
                el.innerHTML = text + item.label;
                el.style.marginTop = '5px';

                this.$refs.myPanel.prepend(el);
            }
        }
    }
</script>

<style>
  
   
</style>