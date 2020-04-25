<template>
  <div class="card">
    <img src="../assets/home.jpg" alt="Home image" class="home-image" />
    <h2 class="title">{{ home.name }}</h2>
    <p class="description">{{ home.description }}</p>
    <button class="button edit-button" @click="clickEdit">
      Edit
    </button>
    <button class="button remove-button" @click="clickRemove">
      Remove
    </button>
  </div>
</template>

<script>
export default {
  name: 'HomeItemList',
  props: {
    home: {
      _id: String,
      name: String,
      imageUrl: String,
      description: String
    }
  },
  methods: {
    clickEdit() {
      alert('Edit clicked');
    },
    clickRemove() {
      alert('Remove clicked');
    }
  }
};
</script>

<style lang="scss" scoped>
.card {
  width: 95%;
  display: flex;
  flex-direction: column;
  background-color: lightgray;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
    Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  margin: auto;
}

.home-image {
  width: 100%;
  height: 250px;
}

.title {
  font-weight: bolder;
  padding-left: 10px;
  font-size: 22pt;
  margin: 10px;
}

.description {
  margin: 0;
  padding: 2%;
}

.button {
  color: white;
  border-color: white;
}

.edit-button {
  background-color: #47ca47;
}

.remove-button {
  background-color: #ff5a5a;
}
</style>
