<template>
  <div id="basicLayout">
      <a-layout>
      <a-layout-header class="header">
        <GlobalHeader />
      </a-layout-header>
      <a-layout-content class="content">
        <router-view />
      </a-layout-content>
      <a-layout-footer class="footer">
        <a href="https://www.antdv.com" target="_blank" rel="noopener noreferrer">
        Ant Design Vue
        </a>
        </a-layout-footer>
      </a-layout>
  </div>
</template>

<script setup lang="ts">
  import GlobalHeader from '@/components/GlobalHeader.vue';
</script>
<!-- <script lang="ts">
export default {
  // component options
}
</script> -->

<style scoped>
#basicLayout .footer{
  background: #67e4c7;
  text-align: center;
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
}
#basicLayout .content{
  margin-bottom: 20px;
  padding: 20px; /* Prevent content from being hidden behind the fixed footer */
  background: linear-gradient(to right, #49c4be, #ffffff);
}
#basicLayout .header{
  background: white;
  margin-bottom: 0px;
  color: unset;
  padding-inline: 20px;
}
</style>
