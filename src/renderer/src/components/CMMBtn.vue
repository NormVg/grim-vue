<script setup>
const ipcCloseApp = () => {
    // alert("close")       

    window.electron.ipcRenderer.send('close-app')
}

const ipcMaxApp = () =>{
    window.electron.ipcRenderer.send('max-app')
    
}

const ipcMinApp = () =>{
    window.electron.ipcRenderer.send("min-app")
}


                
</script>

<template>
    <div id="cmm-box">
        <button @click="ipcMinApp" id="cmm-min-btn"></button>
        <button @click="ipcMaxApp" id="cmm-max-btn"></button>  
        <button @click="ipcCloseApp" id="cmm-close-btn"></button>
    </div>
</template>

<style>

#cmm-box{
    /* border: 1px solid red; */
    display: flex;
    justify-content: space-between;
    align-items: center;

    width: 55px;
    margin-right: 10px;
    position: absolute;
    right: 0px;
    -webkit-app-region: no-drag;
}

#cmm-close-btn{
    background-color: #FF4343;
}

#cmm-max-btn{
    background-color: #08C371;
}
#cmm-min-btn{
    background-color: #FED31D;   
}
button{
    height: 15px;
    width:  15px;
    opacity: 70%;
    border-radius: 20px;
    border: none;
}   

button:hover{
    transition: all ease-in-out 200ms;
    height: 25px;
    opacity: 100%;
}
</style>