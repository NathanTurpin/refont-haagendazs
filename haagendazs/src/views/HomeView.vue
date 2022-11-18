<template>
  <div>
    <TopNav />
    <MainHeader />
    <BotHeader />
    <main>
      <div class="news">
        <h3>Nos nouveautés</h3>
        <!-- <div class="row justify-content-between">
          <div v-for="(card, id) in cards" :key="id" class="col-sm-2">
            <div
              class="card-news"
              @mouseover="displayFullCard(id)"
              @mouseleave="hideCard(id)"
            >
              <div class="images">
                <img
                  :src="require('@/assets/' + card.background)"
                  alt=""
                  class="images__back"
                />
                <img
                  :src="require('@/assets/' + card.image)"
                  class="images__front"
                />
              </div>

              <div class="card-news__body">
                <h6 class="card-news__text">
                  {{ card.title }}
                </h6>
              </div>
            </div>
          </div>
        </div> -->
        <div class="row-news">
          <div v-for="(card, id) in cards" :key="id">
            <div
              class="card-news"
              @mouseover="displayFullCard(id)"
              @mouseleave="hideCard(id)"
            >
              <div class="card-news__images">
                <img
                  :src="require('@/assets/' + card.background)"
                  alt=""
                  class="card-news__images--back"
                />
                <img
                  :src="require('@/assets/' + card.image)"
                  class="card-news__images--front"
                />
              </div>
              <div class="card-news__body">
                <h6 class="card-news__body--text">
                  {{ card.title }}
                </h6>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="crossover">
        <div class="crossover__left">
          <div class="crossover__left--text">
            <h3>Haagen-Dazs x Biscoff</h3>
            <p>
              Lorsque l'onctuosité de la crème glacée au caramel rencontre le
              croquant du Lotus Biscoff, cela crée un mélange irrésistible !
            </p>
            <button>Découvrir Notre collab’ X Biscoff</button>
          </div>
          <div class="crossover__left--img">
            <img src="@/assets/bisscoff1.png" alt="" />
            <img src="@/assets/bisscoff2.png" alt="" />
          </div>
        </div>
        <div class="crossover__right">
          <img
            src="@/assets/back-bisscoff-crossover.png"
            alt=""
            class="crossover__right--bisscoff"
          />
        </div>
      </div>
    </main>
  </div>
</template>

<script setup>
import TopNav from "@/components/TopNav.vue";
import MainHeader from "@/components/MainHeader.vue";
import BotHeader from "@/components/BotHeader.vue";

const cards = [
  {
    title: "Duo Chocolat Noir et Caramel Salé Croquant",
    image: "duo.png",
    background: "back-duo.png",
  },
  {
    title: "Macadamia",
    image: "macadamia-nut-brittel.png",
    background: "back-macadamia-nut-brittel.png",
  },
  {
    title: "Peanut Butter Crunch",
    image: "peanut-butter-crunch.png",
    background: "back-peanut-butter-crunch.png",
  },
  {
    title: "Duo Vanilla Brownie et Framboise",
    image: "white-peach.png",
    background: "back-white-peach.png",
  },
  {
    title: "Creamy Fudge Brownie",
    image: "fudge.png",
    background: "back-fudge.png",
  },
];

const displayFullCard = (id) => {
  const cardsText = document.getElementsByClassName("card-news__body");
  const backImages = document.getElementsByClassName("card-news__images--back");
  cardsText[id].style.visibility = "initial";
  backImages[id].style.visibility = "initial";
};

const hideCard = (id) => {
  const cardsText = document.getElementsByClassName("card-news__body");
  const backImages = document.getElementsByClassName("card-news__images--back");
  cardsText[id].style.visibility = "hidden";
  backImages[id].style.visibility = "hidden";
};
</script>

<style lang="scss" scoped>
.news {
  width: 80%;
  margin: 10% auto 0 auto;
}
.row-news {
  display: flex;
  justify-content: space-between;
}

.card-news__images {
  position: relative;
  &--front {
    position: absolute;
    top: 6rem;
    left: 2.5rem;
  }
  &--back {
    visibility: hidden;
  }
}
.card-news__body {
  visibility: hidden;
  &--text {
    margin: 5rem auto 1rem auto;
    text-align: center;
    width: 60%;
  }
}

.crossover {
  display: flex;
  width: 80%;
  margin: auto;
  &__left {
    width: 50%;
    align-content: center;
  }
  &__right {
    width: 50%;
    background-image: url("@/assets/back-crossover.png");
    background-repeat: no-repeat;
    background-clip: content-box;
    &--bisscoff {
      overflow: hidden;
    }
  }
}
</style>