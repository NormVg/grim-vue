
<script setup>
import { inject } from "vue"
                
const isSpaceTopBar = inject("is-topbar-space")


                                            
</script>

<template>
    <div id="window-box" :style="`height: calc(100vh - ${isSpaceTopBar? '50px' : '20px'} );`">
        <slot>

        </slot>
    </div>
</template>

<style>
#window-box{
    background-color: #252525;
    width: calc(100vw - 20px);
    
    border-radius: 10px;
    
    display: flex;
    justify-content: center;
    align-items: center;

    align-self: flex-end;
    margin-bottom: 10px;

    transition: all 150ms ease-in-out;
}
</style>