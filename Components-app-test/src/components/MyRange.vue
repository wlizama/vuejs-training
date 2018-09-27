<template>
    <div class="range my-bg">
        <div class="input-range">
            <input type="range" v-model="conf.value" :min="conf.min" :max="conf.max" :step="conf.step">
            <span>{{ conf.value }}</span>
        </div>
        <slot></slot>
        <div class="buttons-inc-dec animated bounceIn" v-if="conf.show_incrementals">
            <button @click="rangeIncDec('inc')">+</button>
            <button @click="rangeIncDec('dec')">-</button>
        </div>
    </div>
</template>

<script>
    import styl from "../styles/common.css"

    export default {
        name : "myrange",
        props : {
            conf : {
                // tipos
                value : Number,
                min : {
                    type : Number,
                    default: 0
                },
                max : {
                    type : Number,
                    default: 100
                },
                step : {
                    type : Number,
                    default: 1
                },
                show_incrementals : Boolean
            }
        },
        methods : {
            rangeIncDec (action) {
                if(action === "inc")
                    this.conf.value = parseFloat(this.conf.value) + parseFloat(this.conf.step)
                
                if(action === "dec")
                    this.conf.value = parseFloat(this.conf.value) - parseFloat(this.conf.step)
            }
        }
    }
</script>

<style>
    .range {
        display: flex;
        border: 1px solid #CCC;
        border-radius: 5px;
        padding: 5px;
        flex-direction: column;
        align-items: center;
        max-width: 240px;
    }
    .range .input-range, .range .buttons-inc-dec {
        display: block;

    }
</style>
