<template>
    <div>
      <div class="Contact">
        <p>E-mail: cerovina1997@gmail.com</p>
      </div>
      <div class="image2">
        <img class="pic2" :src="require('../assets/weapon-images/dagger.png')">
      </div>
    </div>
  </template>
  
  <style scoped>
    body {
      background-color: black;
    }
  
    h1 {
      font-size: 20px;
    }
  
    .image2 {
      margin: auto;
    }
  
    p {
      font-size: 20px;
    }
  
    .pic2 {
      width: 30%;
      margin-top: 80px;
      margin-bottom: 30px;
      animation: rotateImages 10s linear infinite;
      transform-style: preserve-3d; /* Enable 3D transformations */
    }
  
    @keyframes rotateImages {
      0% {
        transform: rotateY(0deg);
      }
      100% {
        transform: rotateY(360deg);
      }
    }
  
    @media screen and (max-width: 767px) {
      .pic2 {
        width: 55%;
      }
    }
  </style>
  