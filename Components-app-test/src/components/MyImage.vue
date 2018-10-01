<template>
    <figure>
        <img :src="attrbs.img_src" :alt="attrbs.img_alt_text">
        <figcaption>{{attrbs.caption_text}}</figcaption>
    </figure>
</template>

<script>
    export default {
        name : "myImage",
        props : ["attrbs"]
    }
</script>