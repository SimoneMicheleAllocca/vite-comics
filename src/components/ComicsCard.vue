<script>
export default {
  props: {
    cardImage: String,
    cardTitle: String,
    cardPrice: String,
    cardType: String,
  },
  data() {
    return {
      show: true,
    };
  },
  methods: {
    getVision (event) {
      event.preventDefault(); 
      this.show = !this.show;
    }
  },
};
</script>

<template>
  <div class="card" @click="getVision">
    <div class="front" v-show="show">
      <a href="">
        <img :src="cardImage" alt="" />
      </a>
      <h4>{{ cardTitle }}</h4>
    </div>

    <div class="back" v-show="!show">
      <h4>{{ cardTitle }}</h4>
      <h4>{{ cardType }}</h4>
      <h4>{{ cardPrice }}</h4>
    </div>
  </div>
</template>

<style scoped lang="scss">
@use "../style/partials/_variables.scss" as *;

.card {
  text-align: center;
  width: 200px;
  height: 300px;
  perspective: 1000px;
  position: relative;

  &:hover {
    transform: scale(1.1);
    transition: 1s;
  }

  img {
    max-width: 100%;
    height: 150px;
  }

  h4 {
    color: white;
    font-size: 0.7rem;
    text-transform: uppercase;

    &:hover {
      cursor: pointer;
    }
  }
}
</style>