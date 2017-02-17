<template>
  <!--
  Note: This component is no longer a part of the app. This was one attempt to create a text/photo
  slider that I eventually discarded and replaced with "Plates"
-->
  <div class="component component-a">
    Component A
    <h3>{{this.tab.title}}</h3>
    <p>{{this.tab.text}}</p>
  </div>


</template>

<script>
export default {
props: ['tab'],

data: {
    activeTab: null,
    tabs: [
      {
        title: 'Title A',
        text: 'Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Maecenas scelerisque ac quam vel consectetur. Maecenas tincidunt viverra purus et vestibulum. Donec nec consectetur risus. In id felis vehicula, ultricies leo pharetra, blandit diam. Praesent eu magna sem. Nullam viverra blandit ex, nec eleifend metus ullamcorper ut. Proin mi metus, placerat ac sapien ut, fringilla elementum eros. Vestibulum diam odio, tempor sit amet fermentum vitae, consectetur sit amet nunc. Etiam et fringilla nisl, vel feugiat enim. Pellentesque accumsan imperdiet sapien, vitae efficitur metus lacinia quis. Ut rutrum lacus a ligula laoreet eleifend.',
        componentName: 'firstComponent',
      },
}
</script>

<style>


</style>
