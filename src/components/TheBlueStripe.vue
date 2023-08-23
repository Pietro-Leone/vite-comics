<script>
export default {
  data() {
    return {
      titleImg: [
        {
          title: `digital comics`,
          img: `buy-comics-digital-comics.png`,
        }, {
          title: `dc merchandise`,
          img: `buy-comics-merchandise.png`,
        }, {
          title: `subscription`,
          img: `buy-comics-subscriptions.png`,
        }, {
          title: `comic shop locator`,
          img: `buy-comics-shop-locator.png`,
        }, {
          title: `dc power visa`,
          img: `buy-dc-power-visa.svg`,
        },
      ],
    };
  },
};
</script>

<template>
  <div class="background text-uppercase">
    <div class="container d-flex justify-content-around align-items-center flex-wrap">
      <div v-for="el in titleImg">
        <img :src="`/src/assets/img/${el.img}`" :alt="el.title" class="mx-3 my-5" style="height: 80px; max-width: 80px;">
        <span>{{ el.title }}</span>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.background {
  background-color: $color-primary;
}

span {
  color: white;

}
</style>
