<template>
    <div>
        <div class="info-container">
            <p> Banco Compra <a>1,000,000 USD</a>, yo
                recibo <a>17,160,000 MXN</a>, el dia de <a>HOY.</a></p>
        </div>

        <div class="progress-bar-container">
            <div :style="{ width: progress + '%', height: '100%', borderRadius: '10px', backgroundColor: '#ff9800' }"></div>
        </div>
        <div class="counter-container">
            <i class="fas fa-hourglass-start"></i>
            <div class="time-container">
                <span class="material-symbols-outlined material-icon">
                    hourglass_empty
                </span>
                {{ formatTime(secondsRemaining) }}
            </div>
        </div>
    </div>
</template>
  
<script setup>
import { ref, onMounted } from 'vue';

const secondsRemaining = ref(300);
const progress = ref(0);
let timer = null;

const formatTime = (seconds) => {
    const minutes = Math.floor(seconds / 60);
    const remainingSeconds = seconds % 60;

    return `${String(minutes).padStart(2, '0')}:${String(remainingSeconds).padStart(2, '0')}`;
};

const startTimer = () => {
    timer = setInterval(() => {
        if (secondsRemaining.value > 0) {
            progress.value = 100 - (secondsRemaining.value / 300) * 100;
            secondsRemaining.value -= 1;
        } else {
            clearInterval(timer);
        }
    }, 1000);
};

onMounted(() => {
    startTimer();
});
</script>

  
<style scoped>
p {

    color: #7d808b;
}

a {
    color: #ed8025;
}

.timer-container {
    width: 100px;
    /* Ajusta el ancho según tus necesidades */
    /* Puedes ajustar otros estilos según sea necesario */
}

.progress-bar-container {
    width: calc(250px);
    height: 20px;
    border-radius: 10px;
    overflow: hidden;
    background-color: #f57c00;
    margin-bottom: 10px;
    text-align: center;
    box-sizing: border-box;
    margin: 20px 0px 0 15px;





}



.counter-container {
    display: flex;
    align-items: center;
    font-size: 18px;
}

.counter-container i {
    margin: 5px 10px 10px 10px;
}

.time-container {
    display: flex;
    align-items: center;
    margin: 5px 0px 0px 0px;
    color: #f08125;
}

.material-symbols-outlined {
    font-variation-settings:
        'FILL' 0,
        'wght' 400,
        'GRAD' 0,
        'opsz' 24;
}

.info-container {
    width: calc(250px);
    font-size: 15px;
    border-radius: 10px;
    overflow: hidden;
    margin-bottom: 10px;
    text-align: center;
    box-sizing: border-box;
    margin: 20px 0px 0 15px;
}
</style>