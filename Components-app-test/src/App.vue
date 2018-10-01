<template>
    <section>
        <div class="title-head">{{ title }}</div>
        <MyRange :conf="range_conf">
            <div>
                <a href="#" @click="mostrarIncrementals">{{text_increm}}</a>
            </div>
        </MyRange>

        <MyImage :attrbs="image_conf" />
    </section>
</template>

<script>
    import MyRange from "./components/MyRange.vue"
    import MyImage from "./components/MyImage.vue"
    import "animate.css"
    import my_img from "./images/screenshot01.png"

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
                },
                image_conf : {
                    img_src : my_img,
                    img_alt_text : "Súper Texto alternativo",
                    caption_text : "Tengo 16GB de RAM started pack, pero en la computadora de la oficina :'("
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
