<template>
    <section>
        <div class="title-head">{{ title }}</div>
        <MyRange :conf="range_conf">
            <div>
                <a href="#" @click="mostrarIncrementals">{{text_increm}}</a>
            </div>
        </MyRange>

        <MyImage />
    </section>
</template>

<script>
    import MyRange from "./components/MyRange.vue"
    import MyImage from "./components/MyImage.vue"
    import "animate.css"

    export default {
        name: "mainApp",
        data () {
            return {
                title : "Range Testing",
                text_increm : "Mostrar Incrementales",
                range_conf : {
                    value : 0,
                    // min: 0, 
                    // max: 100,
                    step: 1,
                    show_incrementals: false
                }
            }
        },
        methods : {
            mostrarIncrementals () {
                this.range_conf.show_incrementals = !this.range_conf.show_incrementals
            }
        },
        components : {
            MyRange,
            MyImage
        }
    }
</script>

<style scoped>
    .title-head {
        color: darkorange;
        font-size: 25px
    }
</style>
