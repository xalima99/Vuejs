<template>
    <div class="">
        <input @input="onInput" />
    </div>
</template>

<script>
export default {
    name: 'SearchBar',
    methods: {
        onInput: function(event){
            this.$emit('termChange', event.target.value);
        }
    }
}
</script>

<style scoped>
    input{
        width: 75%;
        border: 1px solid grey;
    }
    div {
        text-align: center;
        margin: 20px;
    }

</style>