<script setup>

import HomeSlot from './components/HomeSlot.vue'
import WindowBox from './components/WindowBox.vue'
import Window from './components/Window.vue'
import TopBar from './components/TopBar.vue'
import SideBarBox from './components/SideBarBox.vue'

import { provide, ref } from 'vue'

const isTopBarSpace = ref(false)
const setTopBarSpace = (val) => {
  isTopBarSpace.value = val
}

const isSideBarMinorSpace = ref(false)
const setSideBarMinorSpace = (val) => {
  isSideBarMinorSpace.value = val
}


const isSideBarMajorSpace = ref(false)
const setSideBarMajorSpace = (val) => {
  isSideBarMajorSpace.value = val
}

provide('is-topbar-space', isTopBarSpace)
provide('set-topbar-space', setTopBarSpace)


provide('is-SideBarMinor-space', isSideBarMinorSpace)
provide('set-SideBarMinor-space', setSideBarMinorSpace)

provide('is-SideBarMajor-space', isSideBarMajorSpace)
provide('set-SideBarMajor-space', setSideBarMajorSpace)


</script>

<template>

  <HomeSlot>
  
    <TopBar />
    <SideBarBox/>
    <WindowBox>
      <Window />
    </WindowBox>
  
  </HomeSlot>

</template>

<style>
</style>
