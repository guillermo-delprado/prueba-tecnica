<template>
    <div class="tabla-seccion">
        <table class="tabla">
            <thead>
                <tr>
                    <th>Proveedor</th>
                    <th></th>
                    <th>Banco Compra</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Dato 1</td>
                    <th>Imagen</th>
                    <td>Dato 2</td>
                </tr>
                <tr>
                    <td>Dato 1</td>
                    <th>Imagen</th>
                    <td>Dato 2</td>
                </tr>
                <tr>
                    <td>Dato 1</td>
                    <th>Imagen</th>
                    <td>Dato 2</td>
                </tr>
                <tr>
                    <td>Dato 1</td>
                    <th>Imagen</th>
                    <td>Dato 2</td>
                </tr>
                <tr>
                    <td>Dato 1</td>
                    <th>Imagen</th>
                    <td>Dato 2</td>
                </tr>
                <tr>
                    <td>Dato 1</td>
                    <th>Imagen</th>
                    <td>Dato 2</td>
                </tr>
                <tr>
                    <td>Dato 1</td>
                    <th>Imagen</th>
                    <td>Dato 2</td>
                </tr>

            </tbody>
        </table>
    </div>
</template>
  
<script setup>

</script>
  
<style scoped>
.tabla-seccion {
    flex: 1;
    padding: 20px;
    overflow: auto;
}

.tabla {
    width: 100%;
    border-collapse: collapse;
    margin-bottom: 20px;
}

.tabla th,
.tabla td {
    padding: 10px;
    border: 1px solid #2b323a;
    text-align: left;
}
</style>
  