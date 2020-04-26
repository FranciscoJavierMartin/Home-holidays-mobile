<template>
  <div id="app">
    <Navbar class="padding-navbar" />
    <div class="list-container">
      <HomeItemList v-for="home in homes" :key="home._id" :home="home" />
    </div>
  </div>
</template>

<script>
import HomeItemList from './components/HomeItemList.vue';
import Navbar from './components/Navbar.vue';

export default {
  name: 'App',
  components: {
    HomeItemList,
    Navbar
  },
  data() {
    return {
      homes: [
        {
          _id: '1',
          name: 'Home 1',
          imageUrl: './assets/home.jpg',
          description:
            'This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool'
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
        },
        {
          _id: '4',
          name: 'Home 4',
          imageUrl: './assets/home.jpg',
          description:
            'This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool'
        },
        {
          _id: '5',
          name: 'Home 5',
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
  margin: 0 auto;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
    Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}

.list-container {
  padding-top: 50px;
  display: flex;
  flex-direction: column;
}
</style>
