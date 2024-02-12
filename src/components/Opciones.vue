<template>
    <div class="botones-seccion">
        <div class="boton">
            <p>Texto 1</p>
            <button @click="onClickBoton1">Botón 1</button>
        </div>
        <div class="boton">
            <p>Texto 2</p>
            <button @click="onClickBoton2">Botón 2</button>
        </div>
        <div class="boton">
            <p>Texto 3</p>
            <button @click="onClickBoton3">Botón 3</button>
        </div>
        <div class="boton">
            <p>Texto 4</p>
            <button @click="onClickBoton4">Botón 4</button>
        </div>
    </div>
</template>
  
<script setup>

</script>
  
<style scoped>
.botones-seccion {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 20px;
    background-color: #f5f5f5;
}

.boton {
    text-align: center;
    margin-bottom: 10px;
}

button {
    padding: 10px;
    cursor: pointer;
    background-color: #4caf50;
    color: white;
    border: none;
    border-radius: 4px;
}
</style>
  