<template>
    <div class="page-title">
        {{title}}
    </div>
</template>

<script>
export default {
    name: 'PageTitle',
    props: {
        title: String
    }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Lobster&display=swap');

.page-title {
    font-family: 'Lobster', sans-serif;
    color: #011832;
    padding: 30px;
    text-align: center;
    font-size: 60px;
    font-weight: 100;
    align-self: end;
}

</style>