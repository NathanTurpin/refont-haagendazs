<template>
  <div class="botHeader">
    <div class="leftSide">
      <img
        src="../assets/glace-header-leftside2.png"
        alt=""
        class="leftSide__image1"
      />
      <img
        src="../assets/glace-header-leftside1.png"
        alt=""
        class="leftSide__image2"
      />
    </div>
    <div class="rightSide">
      <div class="rightSide__block">
        <h1 class="display">Winter-Dazs</h1>
        <p>
          Deux expériences ultra gourmandes de crèmes glacées autour du
          chocolat, du café et du caramel pour le plus grand des plaisirs en
          hiver
        </p>
        <button class="btn btn-outline-light">Découvrir</button>
      </div>
    </div>
  </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.botHeader {
  height: 764px;
  background-color: #d1ae7a;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.leftSide {
  position: relative;
  top: 0;
  left: 0;
  &__image1 {
    position: relative;
    top: 0;
    left: -100px;
    -webkit-animation: spin 16s linear infinite;
    -moz-animation: spin 16s linear infinite;
    animation: spin 16s linear infinite;
  }
  &__image2 {
    position: absolute;
    top: 30px;
    left: 30px;
  }
}
.rightSide {
  color: white;

  &__block {
    text-align: right;
    width: 60%;
    margin: auto;
  }
}
@-moz-keyframes spin {
  100% {
    -moz-transform: rotate(360deg);
  }
}
@-webkit-keyframes spin {
  100% {
    -webkit-transform: rotate(360deg);
  }
}
@keyframes spin {
  100% {
    -webkit-transform: rotate(360deg);
    transform: rotate(360deg);
  }
}
</style>