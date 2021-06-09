<template>
<div>
    <header>
        <a href="#">
            <img src="../assets/spotify.png" alt="spotify_logo">
        </a>
    </header>
</div>
    
</template>

<script>

export default {
    name: "Header",
}
</script>

<style lang="scss">
@import '../style/variables';
    header {
        height: 80px;
        display: flex;
        align-items: center;
        background-color: $backgroundColor;
            & img {
                height: 50px;
                margin-left: 10px;
            }  
    }   
</style>