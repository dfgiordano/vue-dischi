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
header {
    height: 80px;
    display: flex;
    align-items: center;
    background-color: #2E3A46;
        & img {
            height: 50px;
            margin-left: 10px;
        }  
}
</style>