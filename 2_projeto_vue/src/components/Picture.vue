<template>
    <img :src="avatar" :alt="descricao">
</template>

<script>
export default {
    name: 'Picture',
    data() {
        return {
            avatar: "/img/Sonic.png",
            descricao: 'Imagem do Sonic',
        }
    }
}
</script>