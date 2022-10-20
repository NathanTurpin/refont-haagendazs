<template>
  <div class="header">
    <div class="header__logo">
      <img src="../assets/logo.png" alt="" />
    </div>
    <nav class="header__nav">
      <router-link to="/products">Produits</router-link>
      <router-link to="/">Saveurs</router-link>
      <router-link to="/">Notre Histoire</router-link>
      <router-link to="/">Nos Boutiques</router-link>
      <router-link to="/">Devenir Franchisé</router-link>
    </nav>
  </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.header {
  width: 77%;
  margin: auto;
  &__logo {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 35px 0;
  }
  &__nav {
    margin-top: 25px;
    margin-bottom: 25px;
    display: flex;
    justify-content: space-between;
    color: black;
    font-weight: bold;
  }
}
</style>