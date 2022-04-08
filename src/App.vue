<template>
  <div class="container">
    <PageTitle title="Hitung mundur hari raya idul fitri 1443H" />
    <MainBanner :countDownDate='date' :eventName='event' />
    <FooterBar link='https://instagram.com' name='@ferigalung.dev' />
  </div>
</template>

<script>
import MainBanner from './components/MainBanner'
import PageTitle from './components/PageTitle.vue'
import FooterBar from './components/FooterBar.vue'
export default {
  name: 'App',
  components: {
    MainBanner,
    PageTitle,
    FooterBar
  },
  data() {
    return {
      date: null,
      event: ''
    }
  },
  created() {
    this.date = new Date('Apr 10, 2022 13:45:00').getTime();
    this.event = 'Hari Raya Idul Fitri'
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Share+Tech&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Poppins&display=swap');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Poppins', sans-serif;
  background: #f3f3f3;
}

.container {
  width: 100vw;
  height: 100vh;
  display: grid;
  grid-template-rows: 4fr 20fr 1fr;
}
</style>
