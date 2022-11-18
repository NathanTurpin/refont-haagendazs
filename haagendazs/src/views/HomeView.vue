<template>
  <div>
    <TopNav />
    <MainHeader />
    <BotHeader />
    <main>
      <div class="news">
        <h3>Nos nouveautés</h3>
        <div class="row-news">
          <div v-for="(card, id) in cards" :key="id">
            <div
              class="card-news"
              @mouseover="displayFullCard(id)"
              @mouseleave="hideCard(id)"
              data-aos="zoom-in"
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
          <div class="crossover__left--paragraphe">
            <h3>Haagen-Dazs x Biscoff</h3>
            <p class="crossover__left--text">
              Lorsque l'onctuosité de la crème glacée au caramel rencontre le
              croquant du Lotus Biscoff, cela crée un mélange irrésistible !
            </p>
            <button class="crossover__left--btn">
              Découvrir Notre collab’ X Biscoff
            </button>
          </div>
          <div class="crossover__left--img">
            <img src="@/assets/bisscoff1.png" alt="" />
            <img src="@/assets/bisscoff2.png" alt="" id="bisscoff2" />
          </div>
        </div>
        <div class="crossover__right">
          <img
            src="@/assets/crossover-glace.png"
            alt=""
            class="crossover__right--glace"
          />
        </div>
        <img
          src="@/assets/back-bisscoff-crossover.png"
          alt=""
          class="crossover__bisscoff"
          data-aos="fade-down-left"
          data-aos-duration="1000"
          data-aos-delay="250"
          data-aos-anchor-placement="center-bottom"
        />
      </div>
    </main>
  </div>
</template>

<script setup>
import TopNav from "@/components/TopNav.vue";
import MainHeader from "@/components/MainHeader.vue";
import BotHeader from "@/components/BotHeader.vue";
import { onMounted } from "vue";
import AOS from "aos";

onMounted(() => {
  AOS.init();
});

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
  cardsText[id].style.transform = "scale(1.1,1.1)";

  backImages[id].style.visibility = "initial";
  backImages[id].style.transform = "scale(1.1,1.1)";
};

const hideCard = (id) => {
  const cardsText = document.getElementsByClassName("card-news__body");
  const backImages = document.getElementsByClassName("card-news__images--back");
  cardsText[id].style.visibility = "hidden";
  cardsText[id].style.transform = "scale(0,0)";

  backImages[id].style.visibility = "hidden";
  backImages[id].style.transform = "scale(0,0)";
};
</script>

<style lang="scss" scoped>
main {
  overflow: hidden;
}
.news {
  width: 80%;
  margin: 10% auto 6% auto;
}
.row-news {
  display: flex;
  justify-content: space-between;
  margin-top: 2%;
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
    transition: transform 1.3s;
  }
}
.card-news__body {
  visibility: hidden;
  transition: transform 1s;

  &--text {
    margin: 5rem auto 1rem auto;
    text-align: center;
    width: 60%;
  }
}

.crossover {
  display: flex;
  width: 95%;
  float: right;
  position: relative;
  &__bisscoff {
    position: absolute;
    top: -15rem;
    margin-left: 13rem;
  }
  &__left {
    width: 40%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    &--paragraphe {
      margin-left: 10%;
    }
    &--text {
      width: 70%;
    }
    &--btn {
      border: 2px solid #c79952;
      background-color: white;
      color: #c79952;
      padding: 14px 108px;
      font-size: 16px;
      cursor: pointer;
    }
    &--img {
      display: flex;
      flex-direction: column;
      width: 20%;
      margin-top: 10%;
    }
  }
  &__right {
    width: 60%;
    background-image: url("@/assets/back-crossover.png");
    background-size: 100% 100%;
    background-repeat: no-repeat;
    position: relative;
    height: 35rem;
    &--glace {
      position: absolute;
      top: -7rem;
      left: 1rem;
      width: 40%;
      z-index: 20;
    }
  }
}
#bisscoff2 {
  margin-left: 20px;
}
</style>