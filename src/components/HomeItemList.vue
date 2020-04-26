<template>
  <div class="card">
    <div class="home-image">
      <img
        v-if="home.imageUrl"
        :src="home.imageUrl"
        alt="Home image"
        @error="onImageError"
      />
      <img v-else src="@/assets/placeholder.png" alt="Home image" />
    </div>
    <h2 class="title">{{ home.name }}</h2>
    <div class="description">
      <p>{{ home.description }}</p>
    </div>
    <div class="action-buttons">
      <button class="edit-button" v-ripple="'green'" @click="clickEdit">
        Edit
      </button>
      <button class="remove-button" v-ripple="'red'" @click="clickRemove">
        Remove
      </button>
    </div>
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
      console.log('Edit clicked');
    },
    clickRemove() {
      console.log('Remove clicked');
    },
    onImageError() {
      this.home.imageUrl = undefined;
    }
  }
};
</script>

<style lang="scss" scoped>
@import '../assets/scss/variables.scss';

.card {
  margin: 10px auto;
  width: 95%;
  display: flex;
  flex-direction: column;
  background-color: white;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}

.home-image img {
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
  padding: 0 5%;
  @include ellipsis-multiline(18, 1.2, 4, 10);
}

.action-buttons {
  display: flex;
  flex-direction: column;
  padding: 15px 10px;
}

button {
  border: none;
  padding: 12px 18px;
  text-transform: uppercase;
  cursor: pointer;
  color: white;
  box-shadow: 0 0 4px #999;
  outline: none;
  border-color: white;
  padding: 10px 0;
  font-size: 15pt;
  border-radius: 10px;
  margin: 5px;
}

.edit-button {
  background-color: #47ca47;
}

.remove-button {
  background-color: #ff5a5a;
}

@media (min-width: $mid_resolution) {
  .description {
    @include ellipsis-multiline(17, 1.2, 10, 10);
  }
  .action-buttons {
    flex-direction: row;
  }

  .edit-button {
    flex-grow: 1;
  }

  .remove-button {
    flex-grow: 1;
  }
}

@media (min-width: $large_resolution) {
  .card {
    max-width: 1000px;
  }
  .home-image {
    height: 400px;
  }

  .action-buttons {
    justify-content: flex-end;
    flex-direction: row;
  }

  button {
    max-width: 200px;
  }
}
</style>
