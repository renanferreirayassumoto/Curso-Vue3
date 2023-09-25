<template>
  <div>
    <img :src="avatar" :alt="descricao" />
    <MudarImagem @mudar-imagem="trocarImagem" />
  </div>
</template>

<script>
import Reutilizacao from "./Reutilizacao.vue";
import MudarImagem from "./MudarImagem.vue";
export default {
  components: {
    Reutilizacao,
    MudarImagem,
  },
  name: "Picture",
  data() {
    return {
      avatar: "/img/Sonic.png",
      descricao: "Imagem do Sonic",
    };
  },
  methods: {
    trocarImagem() {
      this.avatar = "/img/arara.jpeg";
    },
  },
};
</script>