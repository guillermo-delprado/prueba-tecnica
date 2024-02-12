<template>
    <aside>

        <div class="menu">
            <router-link to="/" class="button router-link-active">

                <span class="material-symbols-outlined material-icons">team_dashboard</span>
                <span class="text">Dashboard</span>

            </router-link>
            <router-link to="/about" class="button">
                <span class="material-symbols-outlined material-icons">
                    article
                </span>
                <span class="text">Bitacora</span>
            </router-link>
            <router-link to="/team" class="button">
                <span class="material-symbols-outlined material-icons">
                    settings_panorama
                </span>
                <span class="text">Clientes</span>
            </router-link>

        </div>

        <div class="flex"></div>

        <div class="menu">
            <router-link to="/settings" class="button">

                <span class="text">Agregar widget</span>
                <span class="material-symbols-outlined material-icons">add</span>

            </router-link>
        </div>
    </aside>
</template>
  
<script setup>
// Importa las dependencias necesarias
import { ref } from 'vue'

  // Puedes eliminar la lógica relacionada con la expansión y contracción del sidebar

</script>
  
<style lang="scss" scoped>
aside {
    display: flex;
    flex-direction: column;
    background-color: var(--dark);
    color: var(--light);
    width: calc(300px);
    min-height: 100vh;
    padding: 1rem;
    transition: 0.2s ease-in-out;


    .flex {
        flex: 1 1 0%;
    }



    .material-icons {
        font-size: 2rem;
        color: var(--light);
        padding: 0 5px;
    }

    &:hover {
        .material-icons {
            color: var(--primary);
        }
    }





    h3,
    .button .text,
    .footer p {
        opacity: 1;
    }

    h3 {
        color: var(--grey);
        font-size: 0.875rem;
        margin-bottom: 0.5rem;
        text-transform: uppercase;
    }

    .menu {
        margin: 0 -1rem;


        .button {

            display: flex;
            align-items: center;
            /* Agregado para centrar contenido horizontalmente */
            text-decoration: none;
            padding: 1rem 5rem;


            .material-icons {
                font-size: 2rem;
                color: var(--light);
            }

            .text {
                color: var(--light);
            }

            &:hover {

                .material-icons,
                .text {}
            }

            &.router-link-exact-active {
                // Cambia al color naranja cuando se hace clic


                .material-icons,
                .text {}
            }
        }
    }

    @media (max-width: 1024px) {
        position: absolute;
        z-index: 99;
    }
}
</style>
  