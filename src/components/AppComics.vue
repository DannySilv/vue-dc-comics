<template>
  <div class="card-container">
    <img :src="comicsObject.thumb" alt="" />
    <h4>{{ comicsObject.series }}</h4>
  </div>
</template>

<script>
export default {
  name: "AppComics",
  props: {
    comicsObject: Object,
  },
};
</script>

<style>
.card-container {
  width: calc(100% / 6 - 10px);
  margin-top: 5%;
}

h4 {
  font-size: 0.7rem;
  color: white;
  margin-top: 10%;
}
</style>
