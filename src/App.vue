<template>
  <div id="app" class="list-container">
    <HomeItemList v-for="home in homes" :key="home._id" :home="home" />
  </div>
</template>

<script>
import HomeItemList from './components/HomeItemList.vue';

export default {
  name: 'App',
  components: {
    HomeItemList
  },
  data() {
    return {
      homes: [
        {
          _id: '1',
          name: 'Home 1',
          imageUrl: './assets/home.jpg',
          description:
            'This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool'
        }
      ]
    };
  }
};
</script>

<style lang="scss">
.list-container {
  display: flex;
  flex-direction: column;
}
</style>
