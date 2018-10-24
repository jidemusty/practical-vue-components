<template>
    <div class="app-modal">
        <div class="app-modal-inner">
            Content
        </div>
    </div>
</template>

<style>
    .app-modal {
        background-color: #141420;
        position: fixed;
        width: 100%;
        height: 100%;
        z-index: 9999;
        top: 0;
        left: 0; 
    }

    .app-modal-inner {
        position: fixed;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        background-color: #FFF;
        padding: 30px;
        width: 90%;
        max-width: 500px;
        border-radius: 3px; 
    }
</style>
