<script setup>
defineProps({
  tabEl: Object,
  currentTab: Number,
});
</script>

<template>
  <template v-if="tabEl.id === currentTab">
    <div class="tab-item">
      <h2 class="tab-item__title">{{ tabEl.title }}</h2>
      <div class="tab-item__img-wrapper">
        <img class="tab-item__img" :src="tabEl.img" />
      </div>
      <p class="tab-item__text">
        {{ tabEl.text }}
      </p>
      <button class="tab-item__btn">Read more</button>
    </div>
  </template>
</template>

<style lang="scss" scoped>
.tab-item {
  background-color: #757575;
  text-align: center;
  padding: 20px;
  border-radius: 15px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
  &__title {
    text-transform: uppercase;
    font-weight: 700;
  }

  &__img {
    width: 100%;
    height: 100%;
  }

  &__img-wrapper {
    width: 350px;
    height: 200px;
    overflow: hidden;
    border-radius: 15px;
  }

  &__btn {
    width: 100%;
    padding: 13px 20px;
    border: none;
    background-color: #e4e4e4;
    text-align: center;
    text-transform: uppercase;
    font-weight: 500;
    cursor: pointer;
    border-radius: 15px;
  }
}
</style>
