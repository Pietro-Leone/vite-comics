<script>
import Header from "./components/TheHeader.vue"
import Card from "./components/TheComicsCard.vue"
import Footer from "./components/TheFooter.vue"
import DcComics from "./db/dc-comics.json"
export default {
  components: {
    Header,
    Card,
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
      <div class="container position-relative">
        <span class="badge text-bg-primary position-absolute">Current Series</span>
        <div class="d-flex flex-wrap">
          <div class="card-box" v-for="element in DcComics">
            <Card :thumb="element.thumb" :price="element.price" :series="element.series" :type="element.type" />
          </div>
        </div>
      </div>
    </div>

  </main>

  <Footer />
</template>

<style>
  .cards-container {
    background-color: #1c1c1c;
    padding: 2rem 0;
  }

.badge {
  top: -3rem;
  border-radius: 0;
  padding: .5rem;
  font-size: 1rem;
}


.card-box {
  margin: 1rem;
}

/* .card-box {
} */
</style>