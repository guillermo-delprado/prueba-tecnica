<template>
    <div class="tabla-seccion">
        <table class="tabla">
            <thead>
                <tr>
                    <th class="provtext">Proveedor</th>
                    <th></th>
                    <th class="provprecio">Banco Compra</th>
                </tr>
            </thead>
            <tbody>
                <tr class="mejor">
                    <th>MEJOR COTIZACION:</th>
                    <th> <img :src="x" alt="Vue" class="logo-image" />
                    </th>
                    <th>17.5610</th>
                </tr>
                <!--<tr v-for="dato in datos" :key="dato.id">
                    <td>{{ dato.dato1 }}</td>
                    <td> <img :src="dato.imagen" class="logo-image" />
                    </td>
                    <td>{{ dato.dato2 }}</td>
                </tr>
                
            -->

                <tr class="text">
                    <td>BANCO INTERNACIONAL X</td>
                    <td> <img :src="x" alt="Vue" class="logo-image" />
                    </td>
                    <td>17.<a>56</a>10</td>
                </tr>

                <tr class="bara">
                    <td>BANCO REGIONAL Y</td>
                    <td> <img :src="y" alt="Vue" class="logo-image" />
                    </td>
                    <td>17.<a>54</a>00</td>
                </tr>

                <tr class="text">
                    <td>INSTITUCION Z</td>
                    <td> <img :src="z" alt="Vue" class="logo-image" />
                    </td>
                    <td>17.<a>55</a>80</td>
                </tr>

                <tr class="text">
                    <td>FINTECH A</td>
                    <td> <img :src="a" alt="Vue" class="logo-image" />
                    </td>
                    <td>17.<a>55</a>81</td>
                </tr>

                <tr class="text">
                    <td>BANCO MEXICANO B</td>
                    <td> <img :src="b" alt="Vue" class="logo-image" />
                    </td>
                    <td>17.<a>58</a>59</td>
                </tr>

                <tr class="text">
                    <td>BANCO USA C</td>
                    <td> <img :src="c" alt="Vue" class="logo-image" />
                    </td>
                    <td>17.<a>55</a>90</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>
  
<script setup>



import x from '../assets/banco_internacional-removebg-preview.png'

import y from '../assets/banco_regional-removebg-preview.png'

import z from '../assets/institucion-z.png'

import a from '../assets/fintech_a-removebg-preview.png'

import b from '../assets/Banco_mexicano_b-removebg-preview.png'

import c from '../assets/banco_usa-removebg-preview.png'

</script>

  
<style scoped>
.provtext {
    color: #f9f9f9;
}

.provprecio {
    color: #2aa866;
}

.tabla-seccion {
    flex: 1;
    padding: 20px;
    width: calc(1000px);
    overflow: auto;
}

.tabla {
    width: 100%;
    border-collapse: collapse;
    margin-bottom: 20px;
    padding: 20px;
    border: 2px solid #444b55;

}

.tabla th,
.tabla td {
    padding: 10px;
    text-align: left;
    text-align: center;

}

.tabla th,
td:nth-child(3) {
    white-space: nowrap;
}

.tabla th,
td:nth-child(1) {
    white-space: nowrap;
}



.tabla tbody tr {
    border: 2px solid #444b55;


}

.mejor {
    background: #f08125;
}

a {
    color: #f08125;
}

.logo-image {
    width: 100px;
    height: 30px;
}

.text {
    color: #fefefe;
}

.bara {
    background: #373e48;
    color: #fefefe;
}

.mejor {
    color: #fefefe;
}
</style>
  