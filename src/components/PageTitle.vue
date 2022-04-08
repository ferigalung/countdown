<template>
    <div class="page-title">
        <h1>{{title}}</h1>
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
.page-title {
    padding: 30px auto;
    text-align: center;
    font-size: 2rem;
    margin: 100px auto;
}
</style>