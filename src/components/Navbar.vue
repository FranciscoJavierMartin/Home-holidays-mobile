<template>
  <nav class="navbar">
    <span class="navbar-toggle" id="js-navbar-toggle" @click="toggle">
      <font-awesome-icon icon="bars" />
    </span>
    <a href="#" class="logo">
      <font-awesome-icon :icon="['fab', 'vuejs']" />
    </a>
    <ul class="main-nav" :class="{ active: isOpen }">
      <li>
        <a href="#" class="nav-links">Home</a>
      </li>
      <li>
        <a href="#" class="nav-links">Owners</a>
      </li>
      <li>
        <a href="#" class="nav-links">Sign up</a>
      </li>
      <li>
        <a href="#" class="nav-links">Sign in</a>
      </li>
      <li>
        <a href="#" class="nav-links">Contact</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      isOpen: false
    };
  },
  methods: {
    toggle() {
      this.isOpen = !this.isOpen;
    }
  }
};
</script>

<style lang="scss" scoped>
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

.navbar {
  font-size: 18px;
  background: transparent;
  background-color: green;
  border: 1px solid rgba(0, 0, 0, 0.2);
  padding-bottom: 10px;
  transition: all 0.6s ease-out;
  z-index: 99;
  top: 0;
  position: fixed;
  width: 100%;
}

.main-nav {
  list-style-type: none;
  display: none;
}

.nav-links,
.logo {
  text-decoration: none;
  color: rgba(255, 255, 255, 0.7);
}

.main-nav li {
  text-align: center;
  margin: 15px auto;
}

.logo {
  display: inline-block;
  font-size: 22px;
  margin-top: 10px;
  margin-left: 20px;
}

.navbar-toggle {
  position: absolute;
  top: 10px;
  right: 20px;
  cursor: pointer;
  color: rgba(255, 255, 255, 0.8);
  font-size: 24px;
}

.active {
  display: block;
}

@media screen and (min-width: 600px) {
  .navbar {
    display: flex;
    justify-content: space-between;
    padding-bottom: 0;
    height: 60px;
    align-items: center;
  }

  .main-nav {
    display: flex;
    margin-right: 30px;
    flex-direction: row;
    justify-content: flex-end;
  }

  .main-nav li {
    margin: 0;
  }

  .nav-links {
    margin-left: 40px;
  }

  .logo {
    margin-top: 0;
  }

  .navbar-toggle {
    display: none;
  }

  .logo:hover,
  .nav-links:hover {
    color: rgba(255, 255, 255, 1);
  }
}
</style>
