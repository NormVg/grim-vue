<script setup>
import back from '../assets/img/arrow-left.png'
import forward from '../assets/img/arrow-right.png'
import reload from '../assets/img/refresh.png'
import dotBtn from '../assets/img/dot-btn.png'
import splitBtn from '../assets/img/Vector.png'




</script>

<template>
  <div id="navbar-box">
    <button><img :src="back" alt="" /></button>
    <button><img :src="reload" alt="" /></button>
    <button><img :src="forward" alt="" /></button>
    <input type="text" name="" id="" />

    <button><img :src="dotBtn" alt="" /></button>
    <button><img :src="splitBtn" alt="" /></button>
  </div>
</template>

<style scoped>
#navbar-box {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: row;
  
  width: 100%;
  height: 30px;
  gap: 10px;
  -webkit-app-region: drag;
}
input {
  height: 30px;
  min-width: 100px;
  width: 50vw;
  border: none;
  background-color: #252525;
  border-radius: 5px;
  color: rgb(182, 182, 182);
  padding-left: 10px;
  padding-right: 10px;
  -webkit-app-region: no-drag;
}

input:focus {
  color: whitesmoke;
  outline: 1px solid #ff5f5f;
}
input:hover {
  border: 1px solid #ff5f5f83;
}
button {
  -webkit-app-region: no-drag;
  height: 30px;
  width: 30px;
  background-color: #252525;

  display: flex;
  justify-content: center;
  align-items: center;
  /* border: 1px solid red; */
  border-radius: 5px;
  opacity: 100%;
}

button img {
  height: 20px;
  width: 20px;
}
button:hover {
  border: 1px solid #ff5f5f83;
}

button:active {
  border: 1px solid #ff5f5f;
  border-radius: 5px;
}
</style>