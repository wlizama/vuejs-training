<template>
    <p>{{ hel }} World!</p>
</template>

<script>
    module.exports = {
        data : function () {
            return {
                hel : "Hello"
            }
        }
    }
</script>

<style scoped>
    p {
        font-size: 2em;
        text-align: center
    }
</style>
