<template>
  <div class="card">
    <a href="#" class="card__img-block">
      <svg class="card__button card__button_top" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em"
        viewBox="0 0 24 24">
        <path fill="#8f8f8f" d="M19 4h-3.5l-1-1h-5l-1 1H5v2h14M6 19a2 2 0 0 0 2 2h8a2 2 0 0 0 2-2V7H6z" />
      </svg>
      <div class="card__img-dark">
        <img class="card__img" src="/avatar_einstein.jpg" alt="avatar">
      </div>
    </a>
    <div class="card__info-block">
      <div class="card__info">
        <p class="card__info-name">Альберд Эйнштейн</p>
        <p class="card__info-proff">Физик-теоретик</p>
      </div>
      <div class="card__buttons">
        <div>
          <svg class="card__button card__button_scale" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em"
            viewBox="0 0 24 24">
            <g fill="none">
              <path fill="#8f8f8f"
                d="m15 14l-.74.123a.75.75 0 0 1 .74-.873zM4 14v.75a.75.75 0 0 1-.75-.75zm16.522-2.392l.735-.147zM6 3.25h11.36v1.5H6zm12.56 11.5H15v-1.5h3.56zm-2.82-.873l.806 4.835l-1.48.247l-.806-4.836zm-.92 6.873h-.214v-1.5h.213zm-3.335-1.67L8.97 15.307l1.248-.832l2.515 3.773zM7.93 14.75H4v-1.5h3.93zM3.25 14V6h1.5v8zm16.807-8.54l1.2 6l-1.47.295l-1.2-6zM8.97 15.308a1.25 1.25 0 0 0-1.04-.557v-1.5c.92 0 1.778.46 2.288 1.225zm7.576 3.405a1.75 1.75 0 0 1-1.726 2.038v-1.5a.25.25 0 0 0 .246-.291zm2.014-5.462a1.25 1.25 0 0 0 1.226-1.495l1.471-.294a2.75 2.75 0 0 1-2.697 3.289zm-1.2-10a2.75 2.75 0 0 1 2.697 2.21l-1.47.295A1.25 1.25 0 0 0 17.36 4.75zm-2.754 17.5a3.75 3.75 0 0 1-3.12-1.67l1.247-.832a2.25 2.25 0 0 0 1.873 1.002zM6 4.75c-.69 0-1.25.56-1.25 1.25h-1.5A2.75 2.75 0 0 1 6 3.25z" />
              <path stroke="#8f8f8f" stroke-width="1.5" d="M8 14V4" />
            </g>
          </svg>
          <svg class="card__button" xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24">
            <g fill="none">
              <path fill="#8f8f8f"
                d="m15 10l-.74-.123a.75.75 0 0 0 .74.873zM4 10v-.75a.75.75 0 0 0-.75.75zm16.522 2.392l.735.147zM6 20.75h11.36v-1.5H6zm12.56-11.5H15v1.5h3.56zm-2.82.873l.806-4.835l-1.48-.247l-.806 4.836zm-.92-6.873h-.214v1.5h.213zm-3.335 1.67L8.97 8.693l1.248.832l2.515-3.773zM7.93 9.25H4v1.5h3.93zM3.25 10v8h1.5v-8zm16.807 8.54l1.2-6l-1.47-.295l-1.2 6zM8.97 8.692a1.25 1.25 0 0 1-1.04.557v1.5c.92 0 1.778-.46 2.288-1.225zm7.576-3.405A1.75 1.75 0 0 0 14.82 3.25v1.5a.25.25 0 0 1 .246.291zm2.014 5.462c.79 0 1.38.722 1.226 1.495l1.471.294A2.75 2.75 0 0 0 18.56 9.25zm-1.2 10a2.75 2.75 0 0 0 2.697-2.21l-1.47-.295a1.25 1.25 0 0 1-1.227 1.005zm-2.754-17.5a3.75 3.75 0 0 0-3.12 1.67l1.247.832a2.25 2.25 0 0 1 1.873-1.002zM6 19.25c-.69 0-1.25-.56-1.25-1.25h-1.5A2.75 2.75 0 0 0 6 20.75z" />
              <path stroke="#8f8f8f" stroke-width="1.5" d="M8 10v10" />
            </g>
          </svg>
        </div>
        <p class="card__likes">3</p>
      </div>
    </div>
  </div>
</template>

<script setup>

</script>

<style scoped>
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