<template>
    <aside>

        <div class="menu">
            <div class="logo">
                <img :src="logoURL" alt="Vue" class="logo-image" />
            </div>

            <router-link to="/" class="button router-link-active">

                <span class="material-symbols-outlined material-icons">team_dashboard</span>
                <span class="text">Dashboard</span>

            </router-link>
            <router-link to="/a" class="button">
                <span class="material-symbols-outlined material-icons">
                    article
                </span>
                <span class="text">Bitacora</span>
            </router-link>
            <router-link to="/a" class="button">
                <span class="material-symbols-outlined material-icons">
                    settings_panorama
                </span>
                <span class="text">Clientes</span>
            </router-link>

        </div>

        <div class="flex"></div>

        <div class="menu">
            <BotonAgregarWidget />
            <Usuario />
        </div>
    </aside>
</template>
  
<script setup>
import { ref } from 'vue'
import logoURL from '../assets/logo.png'
import BotonAgregarWidget from './BotonAgregarWidget.vue'
import Usuario from './Usuario.vue'

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
        font-size: 1.35rem;
        color: var(--light);
        padding: 0 5px;
    }

    .material-symbols-outlined {
        font-size: 1rem;
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
        display: flex;
        align-items: start;
    }

    .menu {
        margin: 0 -1rem;

        .button {

            display: flex;
            align-items: center;
            border-radius: 8px;
            /* Desenfoque en la parte inferior */

            text-decoration: none;
            margin: 1.8rem 4.5rem;
            font-size: 1.2rem;
            padding: .8rem .5rem;


            .material-icons {
                font-size: 1.4rem;
                color: var(--light);
            }

            .text {
                color: var(--light);
            }

            &:hover {
                background: var(--button);
                box-shadow: 0 5px 5px #875630;

                .material-icons,
                .text {}
            }


            &.router-link-exact-active {
                // Cambia al color naranja cuando se hace clic
                background: var(--button);
                box-shadow: 0 3px 5px #875630;

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

.logo {
    display: flex;
    align-items: center;
}

.logo-image {
    width: 300px;
    height: 100px;
}
</style>
  