<template>
    <img :src="avatar" :alt="descricao">
</template>
<script>
export default {
    name: 'Picture',
    data() {
        return{
            avatar: "https://assets.pokemon.com/assets/cms2/img/pokedex/full/354_f2.png",
            descricao: "Banette Mega"
        }
    }
}
</script>
