<template>
  <div>
  <div class="about">
      <div class="box">
        <div class="imageMe">
    <img class="picMe" :src="require('../assets/other-images/slikazaturnir.jpg')">
  </div>
    <div class="text">
        <p>
          Hello there!
          <br>
          Here's a showcase of some of the weapons used in the sport I train - Historical European Martial Arts (HEMA).
          <br>
          All of them are perfectly safe and we're equipped with proper gear, such as a mask, gloves and other.
          <br>
          I hope you find them interesting! 😄
        </p>
      </div>
    </div>
  </div>
</div>
</template>

<style scoped>
  body {
    background-color: black;
  }
  p {
    font-size: 25px;
    font-family: "Cinzel";
  }
  .imageMe {
    display: flex;
  }
  .picMe {
    width: 50%;
    margin-left: auto;
    margin-right: 130px;
  }
  .box {
    margin: auto;
    display: flex;
    margin-top: 50px;
    margin-right: 250px;
  }

  @font-face {
  font-family: 'Cinzel';
  src: url('~@/assets/fonts/Cinzel-VariableFont_wght.ttf') format('truetype');
}

  @media screen and (max-width: 767px) {
      .imageMe {
      display: flex;
      margin: auto;
    }
      .picMe {
      width: 300px;
      margin: auto;
    }

      p {
      font-size: 20px;
    }

    .box {
      width: 200px;
      display:contents;
    }

    .text {
      margin: auto;
      margin-top: 30px;
    }
  }
</style>