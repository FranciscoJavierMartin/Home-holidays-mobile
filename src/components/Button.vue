<template>
  <!--<button class="c-button c-button--red" type="button">
    <div class="c-ripple js-ripple">
      <span class="c-ripple__circle"></span>
    </div>
    Long Button to Stress-Test Ripple Animation
  </button>-->
  <button v-ripple="'blue'">This is a button</button>
</template>

<style lang="scss" scoped>
@import '../assets/scss/variables.scss';

@include button-modifier(#e9573f, red);
</style>
