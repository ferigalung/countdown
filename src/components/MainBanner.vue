<template>
    <div class="banner">
        <h2>Menuju {{eventName}} dalam:</h2>
        <ClockTime :time='time.days' desc='DAYS' />
        <ClockTime :time='time.hours' desc='HOURS' />
        <ClockTime :time='time.minutes' desc='MINUTES' />
        <ClockTime :time='time.seconds' desc='SECONDS' />
    </div>
</template>

<script>
import ClockTime from './ClockTime';

export default {
    name: 'MainBanner',
    components: {
        ClockTime
    },
    props: ['countDownDate', 'eventName'],
    data() {
        return {
            time: {}
        }
    },
    created() {
        const interval = setInterval(() => {
            const distance = this.countDownDate - Date.now();

            this.time.days = Math.floor(distance / (1000 * 60 * 60 * 24));
            this.time.hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            this.time.minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            this.time.seconds = Math.floor((distance % (1000 * 60)) / 1000);

            if (distance < 0) {
                clearInterval(interval);
                this.time.days = 0;
                this.time.hours = 0;
                this.time.minutes = 0;
                this.time.seconds = 0;
            }
        }, 1000);
    }
}
</script>

<style scoped>
.banner {
    margin-top: 100px;
    padding: 20px;
    background:#011832;
    width: 900px;
    height: 300px;
    border-radius: 10px;
    color: #f2f2f2;
    border: 10px solid #a87f1f;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    align-self: start;
    justify-self: center;
}

h2 {
    grid-column: 1/5;
    text-align: center;
}
</style>