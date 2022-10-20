<template>
  <div class="topNav">
    <p class="topNav__item">Rappel de produit</p>
    <p class="topNav__item">
      Extension de rappel de la crème glacée Vanille Häagen-Dazs à d’autres
      produits à base de vanille.
    </p>
    <p class="topNav__item">En savoir plus</p>
  </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.topNav {
  background-color: #5d76a7;
  height: 39px;
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  &__item {
    color: white;
    font-weight: 400;
  }
  &__item:first-child {
    font-weight: 700;
  }
}
</style>