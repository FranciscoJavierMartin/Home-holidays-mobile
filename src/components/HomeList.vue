<template>
  <div class="list-container">
    <HomeItemList v-for="home in homes" :key="home._id" :home="home" />
  </div>
</template>

<script>
import HomeItemList from './HomeItemList.vue';

export default {
  components: {
    HomeItemList
  },
  props: {
    homes: {
      required: true
    }
  }
};
</script>

<style lang="scss" scoped>
.list-container {
  padding-top: 50px;
  display: flex;
  flex-direction: column;
}
</style>
