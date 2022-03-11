<template>
  <div class="character">
    <img class="character__img" :src="data.src" alt="" />
    <h2>{{ data.nombre }}</h2>
  </div>
</template>

<script>
export default {
  name: "MyCharacter",
  props: {
    data: {
      type: Object,
      default: () => {},
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.character {
  display: flex;
  align-items: center;
  color: green;
  margin: 20px;
  &__img {
    border-radius: 50%;
    min-width: 100px;
    width: 8vw;
    margin-right: 1rem;
  }
}
</style>
