<template>
  <div class="header">
    <div class="header__logo">
      <img src="../assets/logo.png" alt="" />
    </div>

    <nav class="navbar navbar-expand-lg header__nav">
      <div class="container-fluid">
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNav"
          aria-controls="navbarNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="header__nav">
            <li class="nav-item">
              <router-link class="nav-link active" to="/products"
                >Produits</router-link
              >
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/">Saveurs</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/">Notre Histoire</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/">Nos Boutiques</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/"
                >Devenir Franchisé</router-link
              >
            </li>
          </ul>
        </div>
      </div>
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
    width: 100%;
    color: black;
    font-weight: bold;
    list-style: none;
    display: flex;
    justify-content: space-evenly;
  }
}
</style>