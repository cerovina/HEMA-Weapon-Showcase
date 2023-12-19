<template>
  <div>
  <div class="about">
      <div textBox>
        <p>
          Hello there!
          <br>
          Here's a showcase of some of the weapons used in the sport I train - Historical European Martial Arts (HEMA).
          <br>
          All of them are perfectly safe and we are equipped with proper gear, such as a mask, gloves and other.
          <br>
          I hope you find them interesting! 😄
        </p>
    </div>
  </div>
  <div class="imageMe">
    <img class="picMe" :src="require('../assets/other-images/slikazaturnir.jpg')">
  </div>
</div>
</template>

<style scoped>
  body {
    background-color: black;
  }
  p {
    font-size: 20px;
  }
  .imageMe {
    margin-right: 560px;
    display: flex;
  }
  .picMe {
    width: 40%;
    margin-left: 400px;
    margin-top: 30px;
    margin-left: auto;
  }
  .textBox {
    width: 200px;
  }
</style>