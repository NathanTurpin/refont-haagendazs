<template>
  <router-view />
</template>

<style lang="scss">
* {
  border: 0;
  margin: 0;
  box-sizing: border-box;
}
body {
  background-color: #fbf4e9;
  font-family: "Reuben";
  font-weight: bold;
  line-height: 150%;
  letter-spacing: auto;
}
a {
  text-decoration: none;
  &:link {
    color: black;
  }
  &:active {
    font-weight: 700;
  }
}
.display {
  font-size: 96px;
}
h1 {
  font-size: 48px;
}
h2 {
  font-size: 40px;
}
h3 {
  font-size: 36px;
  color: #c79952;
}
h4 {
  font-size: 32px;
}
h5 {
  font-size: 24px;
}
h6 {
  font-size: 20px;
}
</style>
