<template>
  <div>
    <nuxt />
  </div>
</template>

<style>
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: inherit;
}

html {
  font-size: 62.5%;
  box-sizing: border-box;
}

body {
  padding: 5rem 5rem 10rem;
  line-height: 1.7;
  font-family: "Nunito Sans", sans-serif;
  color: #555;
  min-height: 100vh;
  background: linear-gradient(to bottom right, #9be15d, #00e3ae);
}

h1 {
  font-family: "Megrim", sans-serif;
  font-size: 6rem;
  color: white;
  transform: skewY(-5deg);
  text-align: center;
  position: relative;
  word-spacing: 3px;
}

h1::before {
  content: "";
  display: block;
  height: 65%;
  width: 49%;
  position: absolute;
  top: 105%;
  left: 50%;
  background: linear-gradient(to bottom, #9be15d, #00e3ae);
  opacity: 0.8;
  z-index: -1;
  transform: skewY(370deg) translate(-50%, -50%);
}
</style>
