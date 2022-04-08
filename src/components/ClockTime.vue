<template>
    <div class="clock-time">
        <div class="time">{{time}}</div>
        <div class="time-desc">{{desc}}</div>
    </div>
</template>

<script>
export default {
    name: 'ClockTime',
    props: {
        time: Number,
        desc: String
    }
}
</script>

<style scoped>
.clock-time {
    color: #F2F2F2;
    font-family: 'Share Tech';
    font-style: normal;
    font-weight: 400;
    font-feature-settings: 'ordn' on;
    text-align: center;
}

.time {
    line-height: 110px;
    font-size: 98px;
    letter-spacing: -0.055em;
}

.time-desc {
    font-size: 20px;
}
</style>