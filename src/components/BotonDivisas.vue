<template>
    <div class="botones-seccion">
        <div class="boton">
            <p>Divisa</p>
            <button @click="onClickBoton1" class="custom-button button">
                MXN - USD
                <span class="material-symbols-outlined">
                    height
                </span></button>
        </div>
        <br>
        <div class="boton">
            <p>Fecha Valor</p>
            <button @click="onClickBoton2" class="custom-button button">Hoy
                <span class="material-symbols-outlined">
                    height
                </span>
            </button>
        </div>
        <br>
        <div class="boton">
            <p>Accion</p>
            <button @click="onClickBoton3" class="custom-button button">
                Banco Compra
                <span class="material-symbols-outlined">
                    height
                </span>
            </button>
        </div>
        <br>
        <div class="boton">
            <p>Importe</p>
            <button @click="onClickBoton4" class="custom-button button">
                <span class="button-text">1,000,000 USD</span>
                <span class="material-symbols-outlined">
                    height
                </span>
            </button>
        </div>
        <div class="boton">
            <BarraDeCarga />
        </div>
        <div class="boton">
            <BotonCotizar />
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'
import BotonCotizar from '../components/BotonCotizar.vue'
import BarraDeCarga from '../components/BarraDeCarga.vue'
</script>



<style scoped>
.boton {
    text-align: start;
}

p {
    color: #d4d5d6;
    margin: 0px 10px 10px 15px;
}

.custom-button {
    font-size: 5px;
    color: #d2d5d8;
    border: 2px solid #28ac67;
    background-color: transparent;
    cursor: pointer;
    transition: background-color 0.3s ease, color 0.3s ease;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
}

.custom-button:hover {

    color: #fff;
}

.button-text {
    text-align: center;
    display: inline-block;
}

.button {
    display: flex;
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
</style>
  