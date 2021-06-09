<template>
<div wrapper>
    <div class="carta">
        <img :src="cd.poster" alt="cover">
        <h3>{{ cd.title }}</h3>
        <h5> {{ cd.author }}</h5>
        <h6> {{ cd.year }}</h6>
    </div>
</div>

    
</template>

<script>
export default {
    name: "Disco",
    props: ["cd"]
}
</script>

<style lang="scss" scoped>
    .carta {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        height: 300px;
        width: 200px;
        margin-bottom: 20px;
        border: 1px solid white;
            h3 {
                text-align: center;;
                text-transform: uppercase;
                font-size: 20px;
                color: white;
            }
            h5 {
                text-align: center;;
                color: #78746D;
                font-size: 16px;
            }
            h6 {
                display: block;
                color: #78746D;
                font-size: 16px;
            }
            img {
                text-align: center;;
                display: inline-block;
                margin-top: 20px;
                height: 100px;
                width: 100px;
            }
    }
    .wrapper {
        display:flex;
    }
</style>