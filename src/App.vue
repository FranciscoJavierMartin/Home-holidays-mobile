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
        },
        {
          _id: '2',
          name: 'Home 2',
          imageUrl: './assets/home.jpg',
          description:
            'This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool'
        },
        {
          _id: '3',
          name: 'Home 3',
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
body {
  background-color: lightblue;
}
.list-container {
  display: flex;
  flex-direction: column;
}
</style>
