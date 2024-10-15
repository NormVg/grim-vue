<script setup>

import { ref } from 'vue';
import WebView from './WebView.vue';

const tabsList = ref(["xyz"])

</script>   

<template>                      
    <div class="window">
       
        
        <WebView v-for="id in tabsList" :key="id"  :TabID="id"/>
            
    </div>
</template>

<style>
.window{
    display: flex;
    justify-content: center;
    align-items: center;

    width: 100%;
    height: 100%;
    gap: 5px;
    overflow: hidden;
    
    flex-direction: row;
}

</style>