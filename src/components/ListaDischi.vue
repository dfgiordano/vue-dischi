<template>
    <div class="background">
        <Select 
        @change="cambiaGenere=scelta()"/>
        <div class="wrapper">
            <div class="disco container">
                <div class="row">
                    <div v-for="disco in dischi" :key="disco.author" class="col-xs-6 col-md-4 col-lg-2">
                        <Disco :cd="disco"/>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Disco from './Disco';
import Select from './Select';
import axios from 'axios';

export default {
    name: "ListaDischi",
    components: {
        Disco,
        Select,
    },
    data: function () {
        return {
            url: 'https://flynn.boolean.careers/exercises/api/array/music',
            dischi: [],
        }
    },
    methods: {
        scelta : function () {
        console.log("cam")
        }
    },   
    created () {
        axios 
            .get(this.url)
            .then(
                (result) => {
                    this.dischi = result.data.response;
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
        flex-wrap: wrap;
        margin : auto;
        height: 80%;
        width: 70%;
    }
</style>