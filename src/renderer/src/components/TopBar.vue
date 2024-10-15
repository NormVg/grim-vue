
<script setup>




import cmmBtn from "./CMMBtn.vue"
import NavBar from "./NavBar.vue"
import { inject, ref } from 'vue'

const setSpaceTopBar = inject('set-topbar-space')

const isFullTopBar = ref(false)
const isTopBarLocked = ref(false)

window.electron.ipcRenderer.send('is-max-app')
window.electron.ipcRenderer.on('is-max-app-reply',(event,data)=>{
  
  isTopBarLocked.value = data

  if (data){
    setTopBar(true)
  }else{
    setTopBar(false)
  }
  
  
})

const setTopBar = (val) => {
    if (isTopBarLocked.value){
      val = true
    }
    isFullTopBar.value = val
    setSpaceTopBar(val)
  

}
</script>

<template>
  <div
    id="topbar"
    :style="`height: ${isFullTopBar ? '35px' : '10px'} ;`"
    @mouseenter ="setTopBar(true)"
    @mouseleave="setTopBar(false)"
  >
  <div v-if="isFullTopBar" id="topbar-inner" >
        <NavBar/>   
      <cmmBtn/>
  </div>
  
  </div>
</template>

<style >
#topbar:hover{
  border: 1px solid red;  
}
#topbar {
  width: 100vw;
  height: 10px;
    background-color: #0D0C0C   ;
  position: fixed;
  top: 0%;
  transition: all 150ms ease-in-out;

  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 10px;
  overflow: hidden;
  
  
  /* background-color: red; */
  /* display: none; */
}

#topbar-inner{
    width: 100%;
    height: 100%;
    border: 1px solid blueviolet;
    border-radius: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    /* padding: 1px; */
    
}

</style>