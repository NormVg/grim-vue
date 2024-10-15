<script setup>

import { defineProps } from 'vue';

defineProps({
    TabID:String
        
})
const testFocuswebview = (val) =>{
// alert(val)
}
</script>

<template>
  <div class="window-webview" :id="TabID">
    <webview @focus="testFocuswebview(TabID)" src="https://google.com" allowpopups></webview>
  </div>
</template>

<style >

.window-webview{
    border: 1px solid #FF5F5F;
    overflow: hidden;
    width: 100%;
    height: calc(100% - 2px);
    border-radius:10px ;
}
webview{
    height: 100%;
    width: 100%;
}
</style>