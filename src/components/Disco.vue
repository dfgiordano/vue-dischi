<template>
    <div class="carta">
        <img :src="cd.poster" alt="cover">
        <h3>{{ cd.title }}</h3>
        <h5> {{ cd.author }}</h5>
        <h6> {{ cd.year }}</h6>
    </div>
</template>

<script>
export default {
    name: "Disco",
    props: ["cd"]
}
</script>

<style lang="scss" scoped>
@import '../style/variables';
    * {
        margin:0;
    }
    .carta {
        display: flex;
        flex-direction: column;
        align-items: center;
        height: 320px;
        width: 180px;
        margin-bottom: 20px;
        background-color: $backgroundColor;
            h3 {
                display:block;
                text-align: center;
                text-transform: uppercase;
                font-size: 22px;
                margin-top: 20px;
                color: $titleColor;
            }
            h5 {
                text-align: center;
                color: $descriptionColor;
                margin-top: 10px;
                font-size: 16px;
            }
            h6 {
                display: block;
                text-align: center;
                color: $descriptionColor;
                font-size: 16px;
            }
            img {
                text-align: center;
                display: block;
                margin-top: 20px;
                height: 140px;
                width: 140px;
            }
    }
</style>