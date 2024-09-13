<script setup>
import HeaderComponent from './components/HeaderComponent.vue';
import CardItem from './components/CardItem.vue';
import FooterComponent from './components/FooterComponent.vue';
import avatarEinstein from '../public/avatar_einstein.jpg'
import avatarLennon from '../public/avatar_lennon.jpg'
import avatarCurie from '../public/avatar_curie.jpg'
import avatarFord from '../public/avatar_ford.jpg'
import avatarMonro from '../public/avatar_monro.jpg'
import avatarEsenin from '../public/avatar_esenin.jpg'
import avatarNapoleon from '../public/avatar_napoleon.jpg'

const users = [
  {
    name: 'Альберд Эйнштейн',
    proff: 'Физик-теоретик',
    avatar: avatarEinstein
  },
  {
    name: 'Джон Леннон',
    proff: 'Музыкант',
    avatar: avatarLennon
  },
  {
    name: 'Мария Кюри',
    proff: 'Ученая',
    avatar: avatarCurie
  },
  {
    name: 'Генри Форд',
    proff: 'Бизнесмен',
    avatar: avatarFord
  },
  {
    name: 'Мэрилин Монро',
    proff: 'Актриса',
    avatar: avatarMonro
  },
  {
    name: 'Сергей Есенин',
    proff: 'Писатель и поэт',
    avatar: avatarEsenin
  },
  {
    name: 'Наполеон Бонапарт',
    proff: 'Император',
    avatar: avatarNapoleon
  },
]


</script>

<template>
  <div class="container">
    <HeaderComponent />
    <main class="main">
      <div class="cards-block">
        <CardItem 
          v-for="user in users"
          :key="user.name"
          :name="user.name"
          :proff="user.proff"
          :avatar="user.avatar"
        />
      </div>
    </main>
    <FooterComponent />
  </div>
</template>

<style scoped>
.container {
  width: 100%;
  max-width: 1280px;
  margin: 0 auto;
  font-weight: normal;
}

.main {
  max-width: 1280px;
}
.cards-block {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 20px;
}

.card__img-block {
  display: block;
  position: relative;
  padding: 0;
}

.card__img {
  object-fit: cover;
  width: 100%;
  height: 400px;
  opacity: 1;
  transition: opacity 124ms linear, transform 124ms linear;
  display: block;
}

.card__img:hover {
  opacity: 0.9;
  transform: scale(1.05);
}

.card__img-dark {
  background: #000;
  overflow: hidden;
}

.card__buttons {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.card__button {
  width: 30px;
  height: 30px;
}

.card__button_top {
  position: absolute;
  top: 15px;
  right: 10px;
  opacity: 50%;
  cursor: pointer;
  z-index: 100;
}

.card__button_scale {
  transform: scaleX(-1);
  margin-top: 15px;
}

.card__info-name {
  font-size: 1.5em;
  font-weight: 500;
}

.card__info-block {
  display: grid;
  grid-template-columns: 4fr 1fr;
  align-items: center;
}

.card__info-proff {
  color: hsla(160, 100%, 37%, 1);
  font-size: 1.1rem;
  font-weight: 400;
  margin: 0;
}

.card__likes {
  font-size: 1.2rem;
}
</style>
