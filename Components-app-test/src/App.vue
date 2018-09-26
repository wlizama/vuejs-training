<template>
    <section>
        <div class="colored" @click="mostrar">{{ textillo }}</div>
        <div v-if="is_mostrar">Lorem ipsum dolor sit amet consectetur adipisicing elit. Ut dolorum quibusdam magnam nesciunt voluptate similique earum provident explicabo hic maxime. Culpa vel debitis qui beatae velit laboriosam, ratione obcaecati veniam?</div>
    </section>
</template>

<script>

    export default {
        name: "mainApp",
        data () {
            return {
                textillo : "lorem",
                is_mostrar : false
            }
        },
        methods : {
            mostrar () {
                this.is_mostrar = !this.is_mostrar
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
