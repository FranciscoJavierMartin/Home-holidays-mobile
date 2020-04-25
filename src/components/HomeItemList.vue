<template>
  <div class="card">
    <img src="../assets/home.jpg" alt="Home image" class="home-image" />
    <h2 class="title">{{ home.name }}</h2>
    <div class="description">
      <p>{{ home.description }}</p>
    </div>
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
@mixin ellipsis-multiline(
  $font-size,
  $line-height,
  $lines-to-show,
  $margin: '0'
) {
  $height-calc: $font-size * $line-height * $lines-to-show;
  display: block;
  display: -webkit-box;
  font-size: $font-size * 1px;
  line-height: $line-height;
  max-height: ($height-calc + $margin) * 1px;
  overflow: hidden;
  position: relative;
  text-overflow: ellipsis;
  -webkit-line-clamp: $lines-to-show;
  -webkit-box-orient: vertical;

  p:not(:first-of-type) {
    display: none;
  }
}

.card {
  max-width: 500px;
  margin: 10px auto;
  width: 95%;
  display: flex;
  flex-direction: column;
  background-color: lightgray;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
    Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
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
  p {
    margin: 10px 0;
  }
  margin: 0;
  padding-left: 2%;
  @include ellipsis-multiline(18, 1.2, 4, 10);
}

.button {
  color: white;
  border-color: white;
  padding-top: 10px;
  padding-bottom: 10px;
  font-size: 15pt;
}

.edit-button {
  background-color: #47ca47;
}

.remove-button {
  background-color: #ff5a5a;
}
</style>
