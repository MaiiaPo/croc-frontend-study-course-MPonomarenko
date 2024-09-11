<template>
  <header class="header">
      <div class="logo">
        <img class="logo__img" src="/logo_ru.png" alt="croc">
        <p class="logo__text">Беру максимум от возможностей</p>
      </div>
      
      <div class="user">
        <div class="user__info">
          <a href="#" class="user__name">
            Альберд Эйнштейн
          </a>
          <p class="user__prof">Физик-теоретик</p>
        </div>
        <img class="user__avatar" src="/avatar_einstein.jpg" alt="avatar"> 
      </div>
    </header>
</template>

<script setup>

</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 40px;
  margin-top: 20px;
  padding-bottom: 10px;
  border-bottom: 1px solid lightgray;
  width: 100%;
}

.user__avatar {
  width: 100px;
  object-fit: cover;
  height: 100px;
  border-radius: 50%;
}

.user__info {
  display: flex; 
  flex-direction: column; 
  align-items: flex-end;  
  padding-right: 10px;
}

.user__name {
  font-size: 1.2rem;
  font-weight: 500;
}

.logo__img {
  width: 100px;
  height: 100%;
}

.logo__text {
  font-size: 1.2rem;
  margin: 0;
}

.user {
  display: flex;
  align-items: center;
}
</style>