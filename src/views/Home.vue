<template>
    <div class="contenedor-externo">
        <div class="cabecera">
            <h5>Divisas</h5>
            <router-link to="/cerrar" class="button">
                <div class="cerrar-btn" @click="cerrarVentana"><span class="material-symbols-outlined ">
                        close
                    </span></div>
            </router-link>
        </div>
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


.cabecera {
    display: flex;
    justify-content: space-between;
    margin-bottom: 10px;
    align-items: center;
    align-items: flex-start;
    width: 100%;


}

.cabecera h5 {
    color: #e98724;
    padding: 5px;
}

.cerrar-btn {
    position: absolute;
    right: 10px;
    cursor: pointer;
    border: none;
    padding: 5px;
    border-radius: 5px;
    color: #8c909a;
}

.contenedor-externo {
    position: relative;
    border-radius: 12px;
    margin: 20px;
    background: #2b323a;
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.contenedor-principal {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 0 10px 10px 10px;
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

h5 {
    color: #e98724;
    margin: 0px 8px;
    display: flex;
    align-items: flex-start;
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