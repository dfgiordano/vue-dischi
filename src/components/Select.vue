<template>
    <form>
        <select name="Generi" id="" v-model="selected"
        @change="$emit('cambiaGenere', selected)">
            <option value="Tutti">Seleziona un genere</option>
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>  
            <option value="Metal">Metal</option>
        </select>
    </form>
</template>

<script>
export default {
    name: "Select",
    data: function() {
        return {
            selected: 'Tutti',
        }
    }
}
</script>

<style>
    select {
        position: absolute;
        left: 50%;
        top: 10%;
        transform: translateX(-50%);
        height: 40px;
        width: 200px;
        border-radius: 5px;
        cursor: pointer;
        outline: none;
        border: 2px solid #45D760;
    }
</style>