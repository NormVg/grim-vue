<template>
<div id="body-box">
    <div id="screen">

        <slot>

        </slot>
    </div>
</div>
</template>


<style>

#screen{
    background-color: #0D0C0C;
    width: 100vw;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    
}
#body-box{
    
    border-radius: 10px;
    overflow: hidden;
}

</style>