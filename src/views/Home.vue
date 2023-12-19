<template>
  <div>
    <h1>HEMA <span class="redTitle">WEAPONS</span></h1>
    <!-- Weapon buttons -->
    <div class="button-grid">
      <div v-for="weapon in weapons" :key="weapon.id" class="button-container">
        <button class="btn" @click="selectWeapon(weapon.id)">{{ weapon.name }}</button>
      </div>
    </div>

    <!-- Display selected weapon details -->
    <div v-if="selectedWeapon" class="weapon-details">
      <img class="pic" :src="require(`@/assets/${selectedWeapon.picture}`)" :alt="Picture" />
        <h2>{{ selectedWeapon.name }}</h2>
        <p class="description">{{ selectedWeapon.description }}</p>
    </div>
  </div>
</template>

<script>
import weaponsData from './weapons.json';

export default {
  data() {
    return {
      weapons: weaponsData.weapons,
      selectedWeaponId: 1, // Set the default selected weapon ID to 1 (Longsword)
    };
  },
  computed: {
    selectedWeapon() {
      return this.weapons.find(weapon => weapon.id === this.selectedWeaponId);
    },
  },
  methods: {
    selectWeapon(weaponId) {
      this.selectedWeaponId = weaponId;
    },
  },
};
</script>

<style>
body {
    background-color: black;
  }
h1 {
  font-size: 4rem;
  margin-right: 770px;
  margin-bottom: 50px;
  margin-top: 10px;
  font-family: "Cinzel";
}
.redTitle {
  color: #dd4132;
}
h2 {
  font-size: 3rem;
  color: white;
  margin-right: 35px;
  padding-top: 75px;
  margin-top: -10px;
  margin-bottom: 0px;
  font-family: "Cinzel";
  font-weight: bold;
  padding: 10px;
  border: 3px #ffe600 solid;
}
.btn {
  width: 150px;
  height: 100px;
  background-color: #EDD5A7;
  font-size: 20px;
  font-family: "Cinzel";
  font-weight: bold;
  border: 3px #ffe600 solid;
}
.btn:hover{
  background-color: #C88F4C;
}
.button-container {
  margin-bottom: 50px;
  width: 33.333%;
}
.button-grid {
  display: grid;
  grid-template-columns: repeat(3, 200px);
  margin-left: 100px;
}
.weapon-details {
  margin-top: -650px;
  margin-left: 800px;
  max-width: 600px;
}
.pic {
  width: 55%;
  margin-bottom: 30px;
  width: 55%;
  animation: rotateImages 10s linear infinite;
  transform-style: preserve-3d; /* Enable 3D transformations */
}
.description {
  font-size: 15spx;
  font-weight: bold;
  color: black;
  max-width: 75%;
  height: 190px;
  margin-top: -10px;
  padding-top: 60px;
  padding-left: 60px;
  padding-right: 60px;
  padding-bottom: 60px;
  justify-content: center;
  align-content: center;
  font-family: "Cinzel";font-family: "Cinzel";
  background-image: url('~@/assets/other-images/pergament.png');
  background-size: contain;
  background-repeat: no-repeat;
}
@keyframes rotateImages {
  0% {
    transform: rotateY(0deg);
  }
  100% {
    transform: rotateY(360deg);
  }
}
@font-face {
  font-family: 'Cinzel';
  src: url('~@/assets/fonts/Cinzel-VariableFont_wght.ttf') format('truetype'); /* Adjust the path to your font file */
}
</style>