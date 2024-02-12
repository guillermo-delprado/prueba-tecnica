<template>
    <div class="contenedor-externo">
        <h1>Divisas</h1>
        <div class="contenedor-principal">
            <div class="contenedor-componentes">
                <div class="botones-contenedor">
                    <Opciones />
                </div>
                <div class="tabla-contenedor">
                    <Tabla />
                </div>

            </div>
        </div>
    </div>
</template>

<script setup>
import Tabla from '../components/Tabla.vue';
import Opciones from '../components/Opciones.vue';
</script>

<style>
body {
    background: #19202a;
}

.contenedor-externo {

    border-radius: 12px;
    margin: 20px;
    background: #2b323a;
    height: 100%;
}

.contenedor-principal {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 10px;
    padding: 10px;
    border-radius: 12px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    border: 2px solid #5b616e;
    background: #2b323a;

}

.contenedor-componentes {
    display: flex;
    flex-direction: row;
}

h1 {
    text-align: center;
    color: #e98724;
}

.botones-contenedor,
.tabla-contenedor {
    flex: 1;
    padding: 10px 0;
}


.tabla-contenedor {
    margin-bottom: 10px;
}
</style>