<script setup>
defineProps({
  currentTab: Number,
});
</script>

<template>
  <div class="tabs-nav">
    <button class="tabs-nav__item" @click="$emit('newTab', (currentTab = 1))">
      Tab #1
    </button>
    <button class="tabs-nav__item" @click="$emit('newTab', (currentTab = 2))">
      Tab #2
    </button>
    <button class="tabs-nav__item" @click="$emit('newTab', (currentTab = 3))">
      Tab #3
    </button>
  </div>
</template>

<style lang="scss" scoped>
.tabs-nav {
  max-width: 1400px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 0 auto;
  margin-top: 40px;
  overflow: hidden;
  border-radius: 15px;
  gap: 5px;
  &__item {
    width: 100%;
    padding: 13px 20px;
    border: none;
    background-color: #e4e4e4;
    text-align: center;
    text-transform: uppercase;
    font-weight: 500;
    cursor: pointer;
  }
}
</style>
