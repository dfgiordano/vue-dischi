<template>
    <div class="carta">
        <a href="#">
            <img :src="cd.poster" alt="cover">
        </a>
        <a href="#">
            <h3>{{ cd.title }}</h3>
        </a>
        <a href="#">
            <h5> {{ cd.author }}</h5>
        </a>
        <a href="#">
            <h6> {{ cd.year }}</h6>
        </a>
        
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
    a {
        text-decoration: none;
    }
    .carta {
        display: flex;
        flex-direction: column;
        align-items: center;
        height: 320px;
        width: calc(100% / 180px);
        margin-bottom: 20px;
        background-color: $backgroundColor;
            h3 {
                display:block;
                text-align: center;
                text-transform: uppercase;
                line-height: 24px;
                font-size: 18px;
                margin-top: 20px;
                color: $titleColor;
                    &:hover {
                        color:#45D760;
                    }
            }
            h5 {
                text-align: center;
                color: $descriptionColor;
                margin: 10px 0;
                font-size: 16px;
                    &:hover {
                        color: white;
                        text-decoration: underline white;

            }
            }
            h6 {
                display: block;
                text-align: center;
                color: $descriptionColor;
                font-size: 14px;
                    &:hover {
                        color: white;
                        text-decoration: underline white;

            }
            }
            img {
                text-align: center;
                display: block;
                margin-top: 20px;
                height: 140px;
                width: 140px;
                    &:hover {
                        opacity: 0.5;
                    }
            }
    }
</style>