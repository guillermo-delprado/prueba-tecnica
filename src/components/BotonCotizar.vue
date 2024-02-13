<template>
    <div class="nuevo-boton">
        <button class="naranja-button" @click="onClickBotonNaranja">
            <span class="button-text">Cotizar</span>
        </button>
    </div>
</template>

<script setup>
import { ref } from 'vue'

</script>

<style scoped>
.nuevo-boton {
    text-align: center;
    margin-top: 20px;
}

.naranja-button {
    background-color: #f08125;
    color: #fff;
    font-size: 1.2rem;
    padding: 0.5rem 1rem;
    width: auto;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    transition: background-color 0.3s ease, color 0.3s ease;
    box-sizing: border-box;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 8px;
    text-decoration: none;
    align-items: center;
    margin: 0px 0px 0 15px;
    font-size: 1rem;
    padding: .5rem .5rem;
    width: calc(250px);
    text-align: center;
    box-sizing: border-box;
}

.button-text {
    text-align: center;
    display: inline-block;
}

.naranja-button:hover {
    background-color: darkorange;
}
</style>