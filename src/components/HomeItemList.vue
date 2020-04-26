<template>
  <div class="card">
    <div class="home-image">
      <img
        v-if="home.imageUrl"
        :src="home.imageUrl"
        alt="Home image"
        @error="onImageError"
      />
      <img v-else src="@/assets/home.jpg" alt="Home image" />
    </div>
    <h2 class="title">{{ home.name }}</h2>
    <div class="description">
      <p>{{ home.description }}</p>
    </div>
    <div class="action-buttons">
      <button class="button edit-button ripple" @click="clickEdit">
        Edit
      </button>
      <button class="button remove-button ripple" @click="clickRemove">
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
  padding-left: 5%;
  padding-right: 5%;
  @include ellipsis-multiline(18, 1.2, 4, 10);
}

.action-buttons {
  display: flex;
  flex-direction: column;
  padding-top: 15px;
  padding-left: 10px;
  padding-right: 10px;
  padding-bottom: 15px;
}

.button {
  color: white;
  border-color: white;
  padding-top: 10px;
  padding-bottom: 10px;
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

.ripple {
  background-position: center;
  transition: background 0.8s;
}
.ripple:hover {
  background: #47a7f5 radial-gradient(circle, transparent 1%, #47a7f5 1%)
    center/15000%;
}
.ripple:active {
  background-color: #6eb9f7;
  background-size: 100%;
  transition: background 0s;
}

button {
  border: none;
  border-radius: 2px;
  padding: 12px 18px;
  font-size: 16px;
  text-transform: uppercase;
  cursor: pointer;
  color: white;
  background-color: #2196f3 !important;
  box-shadow: 0 0 4px #999;
  outline: none;
}

@media (min-width: 768px) {
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

@media (min-width: 992px) {
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

  .button {
    max-width: 200px;
  }
}
</style>
