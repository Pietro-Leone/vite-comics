<script>
import Header from "./components/TheHeader.vue"
import Card from "./components/TheComicsCard.vue"
import BlueStripe from "./components/TheBlueStripe.vue"
import Footer from "./components/TheFooter.vue"
import DcComics from "./db/dc-comics.json"
export default {
  components: {
    Header,
    Card,
    BlueStripe,
    Footer,
  },
  data() {
    return {
      DcComics,
    }
  }
}
</script>

<template>
  <Header />

  <main>

    <div class="cards-container">
      <div class="container position-relative d-flex justify-content-center align-items-end">
        <div class="badge current text-bg-primary position-absolute">Current Series</div>
        <div class="d-flex flex-wrap justify-content-center mb-5">
          <div class="card-box" v-for="element in DcComics">
            <Card :thumb="element.thumb" :price="element.price" :series="element.series" :type="element.type" />
          </div>
        </div>
        <div class="badge text-bg-primary position-absolute">Load more</div>
      </div>
    </div>

    <BlueStripe />

  </main>

  <Footer />
</template>

<style>
.cards-container {
  background-color: #1c1c1c;
  padding: 2rem 0;
  text-transform: uppercase;
}

.badge {
  border-radius: 0;
  padding: .5rem;
  font-size: 1rem;
}

.current {
  top: -3rem;
  left: 0;
}

.card-box {
  margin: 1rem;
}
</style>