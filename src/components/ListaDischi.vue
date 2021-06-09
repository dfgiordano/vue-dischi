<template>
    <div class="background">
        <div class="wrapper">
            <div class="disco">
                <div class="row">
                    <div class="col-6 col-md-4 col-lg-2 col-offset-lg-1">
                        <Disco />
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Disco from './Disco';
import axios from 'axios';

export default {
    name: "ListaDischi",
    components: {
        Disco,
    },
    data: function () {
        return {
            url: 'https://flynn.boolean.careers/exercises/api/array/music',
            dischi: [],
        }
    },
    created () {
        axios 
            .get(this.url)
            .then(
                (result) => {
                    console.log(result.data)
                    this.dischi = result.data;
                } 
            )
    }
}
</script>

<style lang="scss">
    .background {
        display: flex;
        height: calc(100vh - 80px);
        background-color: #1E2D3B;
    }
    .wrapper {
        display: flex;
        justify-content: center;
        margin : auto;
        height: 80%;
        width: 65%;
        background-color: white;
    }
</style>