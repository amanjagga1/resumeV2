<template>
  <tabs alignment="right" layout="top" is-pulled-right animation="slide" :only-fade="false">
    <tab-pane label="About" selected><home></home></tab-pane>
    <tab-pane label="Experience"><experience></experience></tab-pane>
    <tab-pane label="Skills"><skills></skills></tab-pane>
  </tabs>
</template>

<script>
import { Tabs, TabPane } from 'vue-bulma-tabs'
import Home from './home/Home.vue'
import Experience from './experience/Experience.vue'
import Skills from './skills/Skills.vue'

export default {
  components: {
    Tabs,
    TabPane,
    Home,
    Experience,
    Skills
  }
}
</script>

<style lang="scss">
    @import '~bulma/sass/utilities/initial-variables';
    $text: rgba(255,255,255,.5);
    $text-strong: #fff;
    $tabs-link-hover-color: #fff;
    $tabs-border-bottom-width: 3px;
    $tabs-border-bottom-color: #333;
    $tabs-link-hover-border-bottom-color:  rgba(255,255,255,.5);
    $title-color: $text-strong;
    $subtitle-color: $text;
    $timeline-header-width: 8em;
    $link-hover: $text-strong;
    
    @import '~bulma/bulma';
    @import '~animate.css/animate.min.css';
    @import '~bulma-timeline/timeline';
    //body { background-color: #333 };
    body { background-color: #232020; background-image: url(./assets/texture.png)};
    .vue-bulma-tabs { min-height: 100vh};
    .tabs span {font-weight: bold; font-size: 24px;};
    //.tab-pane {height:88vh};
</style>
