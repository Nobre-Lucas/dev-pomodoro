<template>
    <div class="tasks column">
        <h2 class="subtitle">Tarefas</h2>
        <img class="img" src="../assets/cronometro.png" alt="">
        <a class="timer">{{ zfill(hour) }}:{{ zfill(min) }}:{{ zfill(sec) }}</a>

        <div class="btns">
            <button class="btn btn-margin" @click="play">{{ timer !== null ? "PAUSAR" : "VAI" }}</button>
            <button class="btn btn-margin" @click="clear">LIMPAR</button>
        </div>

        <div class="interval" v-show="intervalList.length > 0">
            <ul>
                <li v-for="interval in intervalList" :key="interval">VOCÊ PAUSOU EM {{ interval }}</li>
            </ul>
            <button class="btn" @click="clearIntervalList">LIMPAR HISTÓRICO</button>
        </div>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'TaskContainer',
    data() {
        return {
            sec: 0,
            min: 0,
            hour: 0,
            timer: null as number | null,
            intervalList: [],
        }
    },
    methods: {
        zfill(num: number) {
            return num.toString().padStart(2, '0');
        },
        play() {
            if (this.timer == null) {
                this.playing()
                this.timer = setInterval(() => this.playing(), 1000)
            } else {
                clearInterval(this.timer);
                this.timer = null;
                this.pause();
            }
        },
        playing() {
            this.sec++
            if (this.sec >= 59) {
                this.sec = 0;
                this.min++;
            }
            if (this.min >= 59) {
                this.min = 0;
                this.hour++;
            }
        },
        pause() {
            console.log(this.intervalList)
        },
        clear() {
            if (this.timer !== null) {
                clearInterval(this.timer)
                this.timer = null
            }
            this.sec = 0;
            this.min = 0;
            this.hour = 0;
            this.clearIntervalList();
        },
        clearIntervalList() {
            this.intervalList = []
            console.log(this.intervalList)
        }
    }
})
</script>

<style>
.tasks {
    display: flex;
    width: 100%;
    height: 100vh;
    align-items: center;
    flex-direction: column;
    background-color: #00d1b2;
}

.img {
    width: 75%;
    height: 50vh;
}

.timer {
    color: #fff;
    font-size: 70px;
    margin-top: -210px;
}

.btns {
    margin-top: 155px;
    display: flex;
}

.btn {
    -webkit-user-select: none;
    -moz-user-select: none;

    width: 150px;
    background-color: #fff;
    font-size: 20px;
    border: none;
    border-radius: 5px;
    text-align: center;
    padding: 6px;
    cursor: pointer;
    transition: all ease-in-out .3s;
}

.btn-margin {
    margin: 0px 7px;
}

.btn:hover {
    opacity: 0.8;
}

.interval {
    color: #fff;
    flex: 1;
    width: 420px;
    margin-top: 15px;
}

.interval ul {
    text-align: center;
}

.interval ul li {
    list-style: none;
    background-color: rgb(70, 70, 70);
    padding: 15px;
    margin-bottom: 10px;
}</style>