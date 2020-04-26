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

<style lang="sass" scoped>
@import '../assets/scss/variables.scss';

.list-container
  padding-top: $navbar_height
  display: flex
  flex-direction: column

@media screen and (min-width: $mid_resolution)
  .list-container
    padding-top: $navbar_height_mid
</style>
