<template>
  <div>
    <div>Default</div>
    <JqxButton :theme="'material'"Group :mode="'checkbox'">
      <button style="padding: 4px 16px" value='Left'></button>
      <button style="padding: 4px 16px" value='Center'></button>
      <button style="padding: 4px 16px" value='Right'></button>
    </JqxButtonGroup>
    <br />

    <div>Primary</div>
    <JqxButton :theme="'material'"Group :mode="'checkbox'" :template="'primary'">
      <button style="padding: 4px 16px" value='Left'></button>
      <button style="padding: 4px 16px" value='Center'></button>
      <button style="padding: 4px 16px" value='Right'></button>
    </JqxButtonGroup>
    <br />

    <div>Success</div>
    <JqxButton :theme="'material'"Group :mode="'checkbox'" :template="'success'">
      <button style="padding: 4px 16px" value='Left'></button>
      <button style="padding: 4px 16px" value='Center'></button>
      <button style="padding: 4px 16px" value='Right'></button>
    </JqxButtonGroup>
    <br />

    <div>Info</div>
    <JqxButton :theme="'material'"Group :mode="'checkbox'" :template="'info'">
      <button style="padding: 4px 16px" value='Left'></button>
      <button style="padding: 4px 16px" value='Center'></button>
      <button style="padding: 4px 16px" value='Right'></button>
    </JqxButtonGroup>
    <br />

    <div>Warning</div>
    <JqxButton :theme="'material'"Group :mode="'checkbox'" :template="'warning'">
      <button style="padding: 4px 16px" value='Left'></button>
      <button style="padding: 4px 16px" value='Center'></button>
      <button style="padding: 4px 16px" value='Right'></button>
    </JqxButtonGroup>
    <br />

    <div>Danger</div>
    <JqxButton :theme="'material'"Group :mode="'checkbox'" :template="'danger'">
      <button style="padding: 4px 16px" value='Left'></button>
      <button style="padding: 4px 16px" value='Center'></button>
      <button style="padding: 4px 16px" value='Right'></button>
    </JqxButtonGroup>
  </div>
</template>

    <script>

    import JqxButtonGroup from 'jqwidgets-scripts/jqwidgets-vue/vue_jqxbuttongroup.vue';

    export default {
        components: {
            JqxButtonGroup
        }
    }
</script>

<style>
     
  
</style>