<template>
    <section>
        <div class="colored">{{ textillo }}</div>
    </section>
</template>

<script>

    export default {
        name: "mainApp",
        data () {
            return {
                textillo : "lorem"
            }
        }
    }
</script>

<style>
    .colored {
        color: darkorange;
        font-size: 25px
    }
</style>
