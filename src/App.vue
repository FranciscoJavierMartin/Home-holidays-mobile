<template>
  <div id="app">
    <Navbar />
    <HomeList :homes="this.homes" />
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
            'https://r-cf.bstatic.com/images/hotel/max1024x768/235/235711271.jpg',
          description:
            'This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool'
        },
        {
          _id: '2',
          name: 'Home 2',
          imageUrl: 'No image',
          description:
            'This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool'
        },
        {
          _id: '3',
          name: 'Home 3',
          imageUrl:
            'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTMj4JEpbztcLXDzthPc6JQeO-tId8u-iaLtaubOlKJdTdw6tt6&s',
          description:
            'This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool'
        },
        {
          _id: '4',
          name: 'Home 4',
          imageUrl:
            'https://mattamyhomes.com/~/media/images/mattamywebsite/corp/home/heroslideshow/usa/orlando/orl_geohero_02_1600x800.jpg',
          description:
            'This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool'
        },
        {
          _id: '5',
          name: 'Home 5',
          imageUrl:
            'https://r-cf.bstatic.com/images/hotel/max1024x768/235/235711271.jpg',
          description:
            'This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool. This house count with two bedrooms, four bathrooms and garden. Kids can play in the swimming pool'
        }
      ]
    };
  }
};
</script>

<style lang="sass">
@import './assets/scss/variables.scss';

body
  background-color: $main_background_color
  margin: 0 auto
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif
</style>
