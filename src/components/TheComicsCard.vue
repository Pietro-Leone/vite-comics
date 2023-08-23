<script>
export default {
  props: {
    thumb: String,
    price: String,
    series: String,
    type: String,
  }
}
</script>

<template>
  <div class="card">
    <div class="position-relative title-hover">
      <img :src="thumb" :alt="series">
      <div class="position-absolute opacity-0 d-flex justify-content-center w-100 title-price">{{ price }}</div>
      <div class="position-absolute opacity-0 d-flex justify-content-center w-100 title-type">{{ type }}</div>
    </div>
    <span>{{ series }}</span>
  </div>
</template>

<style lang="scss" scoped>
.card {
  background-color: transparent;
  color: white;
  border: 0;
}

.title-hover:hover{
  background-color: black;
  img{
    opacity: .2;
  }
  .title-type, .title-price{
    opacity: 1!important;
    font-size: large;
    font-weight: bold;
  }
}

img {
  height: 180px;
  aspect-ratio: 1/1;
  object-fit: cover;
  object-position: top;
}

.title-type {
  top: 0;
}

.title-price {
  bottom: 0;
}

span {
  max-width: 180px;
  height: 50px;
}
</style>