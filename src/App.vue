<template>
  <div id="app">
    <Navbar class="padding-navbar" />
    <HomeList :homes="homes" />
  </div>
</template>

<script>
import HomeList from './components/HomeList.vue';
import Navbar from './components/Navbar.vue';

export default {
  name: 'App',
  components: {
    HomeList,
    Navbar
  },
  data() {
    return {
      homes: [
        {
          _id: '1',
          name: 'Home 1',
          imageUrl:
            'https://miro.medium.com/max/1200/1*mk1-6aYaf_Bes1E3Imhc0A.jpeg',
          description:
            'This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool'
        },
        {
          _id: '2',
          name: 'Home 2',
          imageUrl:
            'https://miro.medium.com/max/1200/1*mk1-6aYaf_Bes1E3Imhc0A.jpeg',
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
</style>
