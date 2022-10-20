<template>
  <div class="botHeader">
    <div class="botHeader__leftside">
      <img src="../assets/glace-header-leftside2.png" alt="" />
      <img src="../assets/glace-header-leftside1.png" alt="" />
    </div>
    <div class="botHeader__rightside">
      <div>
        <h1>Winter-Dazs</h1>
        <p>
          Deux expériences ultra gourmandes de crèmes glacées autour du
          chocolat, du café et du caramel pour le plus grand des plaisirs en
          hiver
        </p>
        <button>Découvrir</button>
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
  &__leftside {
    width: 50%;
  }
  &__rightside {
    color: white;
    div {
      width: 71%;
      text-align: right;
      h1 {
        font-size: 80px;
      }
    }
  }
}
</style>