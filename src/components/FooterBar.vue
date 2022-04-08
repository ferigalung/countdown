<template>
    <div class="footer">
        created by <a :href="link" target="_blank">{{name}}</a>
    </div>
</template>

<script>
export default {
    name: 'FooterBar',
    props: ['link', 'name']
}
</script>

<style scoped>
.footer {
    color: #f3f3f3;
    background: #a87f1f;
    padding: 10px 30px;
    align-self: center;
    font-weight: bold;
}

.footer a {
    padding: 5px;
    border-radius: 5px;
    text-decoration: none;
    color: #011832;
    cursor: pointer;
}

.footer a:hover {
    color: #f3f3f3;
    background: #011832;
}
</style>