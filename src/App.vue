<template>
  <div id="app">
    <div>
      <MyCharacter
        v-for="character in characterData"
        :key="character.name"
        :data="character"
      />
    </div>
  </div>
</template>

<script>
import MyCharacter from "./components/MyCharacter.vue";

export default {
  name: "App",
  components: {
    MyCharacter,
  },
  data() {
    return {
      characterData: [
        {
          nombre: "Rick Sanchez",
          src: "https://rickandmortyapi.com/api/character/avatar/1.jpeg",
        },
        {
          nombre: "Morty Smith",
          src: "https://rickandmortyapi.com/api/character/avatar/2.jpeg",
        },
        {
          nombre: "Summer Smith",
          src: "https://rickandmortyapi.com/api/character/avatar/3.jpeg",
        },
        {
          nombre: "Beth Smith",
          src: "https://rickandmortyapi.com/api/character/avatar/4.jpeg",
        },
        {
          nombre: "Jerry Smith",
          src: "https://rickandmortyapi.com/api/character/avatar/5.jpeg",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
body {
  background: url("https://rickandmortypod.com/wp-content/uploads/2018/11/cropped-RM_page-header_background1-3.png");
  background-size: cover;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
  justify-content: space-around;
}
</style>
