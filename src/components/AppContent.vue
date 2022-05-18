<template>
  <div class="menu-container">
    <div class="banner">
      <button class="btn">Current Series</button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
$blue: #0282f9;

.menu-container {
  width: 100%;
  height: 500px;
  margin: 0 auto;
  .banner {
    width: 100%;
    height: 200px;
    background-image: url("../assets/img/jumbotron.jpg");
    background-size: cover;
    background-position: center;
    background-position-y: 0;
    position: relative;
  }
}

.btn {
  color: white;
  background-color: $blue;
  border: 2px solid $blue;
  padding: 0.05rem 0.8rem;
  font-family: "Koulen", cursive;
  position: absolute;
  margin-left: 15%;
  bottom: -15px;
}
</style>
