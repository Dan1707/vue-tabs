<script setup>
import TabsItem from "./TabsItem.vue";
import TabsNav from "./TabsNav.vue";

import { ref } from "vue";

const currentTab = ref(1);
const tabsArray = ref([
  {
    id: 1,
    title: "Tabs title #1",
    text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ducimus sit rerum sunt et tenetur, repellendus labore molestiae laborum nobis temporibus repudiandae sed esse dolorem in enim voluptas obcaecati cupiditate vitae!",
    img: "https://static.vecteezy.com/vite/assets/photo-masthead-375-b8ae1548.webp",
  },
  {
    id: 2,
    title: "Tabs title #2",
    text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ducimus sit rerum sunt et tenetur, repellendus labore molestiae laborum nobis temporibus repudiandae sed esse dolorem in enim voluptas obcaecati cupiditate vitae!",
    img: "https://img.freepik.com/premium-photo/serene-mountain-lake-surrounded-by-pine-trees-realistic-hyperdetailed-rendering_899449-32271.jpg",
  },
  {
    id: 3,
    title: "Tabs title #3",
    text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ducimus sit rerum sunt et tenetur, repellendus labore molestiae laborum nobis temporibus repudiandae sed esse dolorem in enim voluptas obcaecati cupiditate vitae!",
    img: "https://i0.wp.com/picjumbo.com/wp-content/uploads/camping-on-top-of-the-mountain-during-sunset-free-photo.jpg?w=600&quality=80",
  },
]);

const changeTabs = (tab) => {
  currentTab.value = tab;
};
</script>

<template>
  <section class="tabs">
    <TabsNav @new-tab="changeTabs" :currentTab="currentTab" />
    <div class="tabs__container">
      <TabsItem
        v-for="tab in tabsArray"
        :key="tab"
        :tabEl="tab"
        :currentTab="currentTab"
      />
    </div>
  </section>
</template>

<style lang="scss" scoped>
.tabs {
  &__container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 20px;
    max-width: 1400px;
    margin: 0 auto;
    margin-top: 30px;
  }
}
</style>
