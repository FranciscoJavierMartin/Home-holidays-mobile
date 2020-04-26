<template>
  <nav class="navbar">
    <span class="navbar-toggle" id="js-navbar-toggle" @click="toggle">
      <font-awesome-icon icon="bars" />
    </span>
    <a href="#" class="logo">
      <font-awesome-icon :icon="['fab', 'vuejs']" />
    </a>
    <ul class="main-nav" :class="{ active: isOpen }">
      <li v-ripple="'#2196f3'" v-for="route in routes" :key="route.text">
        <a href="route.link" class="nav-links">{{ route.text }}</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false,
      routes: [
        {
          text: 'Home',
          link: '#'
        },
        {
          text: 'Owners',
          link: '#'
        },
        {
          text: 'Sign up',
          link: '#'
        },
        {
          text: 'Sign in',
          link: '#'
        },
        {
          text: 'Contact',
          link: '#'
        }
      ]
    };
  },
  methods: {
    toggle() {
      this.isOpen = !this.isOpen;
    }
  }
};
</script>

<style lang="sass" scoped>
@import '../assets/scss/variables.scss'

*
  box-sizing: border-box
  padding: 0
  margin: 0
  color: white

.navbar
  font-size: 18px
  background-color: $main_color
  border: 1px solid rgba(0, 0, 0, 0.2)
  padding-bottom: 10px
  z-index: 1
  top: 0
  position: fixed
  width: 100%

.main-nav
  list-style-type: none
  display: none

.nav-links,
.logo
  text-decoration: none

.main-nav li
  text-align: center
  margin: 15px auto

.logo
  display: inline-block
  font-size: 22px
  margin-top: 10px
  margin-left: 20px

.navbar-toggle
  position: absolute
  top: 10px
  right: 20px
  cursor: pointer
  font-size: 24px


.active
  display: block


@media screen and (min-width: $mid_resolution)
  .navbar
    display: flex
    justify-content: space-between
    padding-bottom: 0
    height: $navbar_height_mid
    align-items: center

  .main-nav
    display: flex
    margin-right: 30px
    flex-direction: row
    justify-content: flex-end

  .main-nav li
    margin: 0

  .nav-links
    margin-left: 40px

  .logo
    margin-top: 0

  .navbar-toggle
    display: none
</style>
