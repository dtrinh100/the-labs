<template>
  <main class="labs-homepage" role="img" aria-label="Picture of a toy">
    <section class="search-container">
      <h1 class="search-container__header">Search The Labs</h1>
      <ProductSearch :reset="true" />
    </section>
  </main>
</template>

<script>
import ProductSearch from "@/components/ProductSearch";
export default {
  name: "BaseHome",
  components: {
    ProductSearch
  }
};
</script>
<style scoped>
.labs-homepage {
  background: url(../assets/img/home-mobile-bg.jpg) no-repeat center center
    fixed;
  background-size: cover;
  display: grid;
  justify-content: center;
  align-content: center;
  height: 100vh;
}
.search-container {
  background-color: rgba(255, 194, 32, 0.9);
  height: 15rem;
  width: 19rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  color: white;
}
.search-container__header {
  margin-bottom: 2rem;
}

@media only screen and (min-width: 660px) {
  .labs-homepage {
    background: url(../assets/img/home-bg.jpg) no-repeat center center fixed;
    background-size: cover;
  }
  .search-container {
    width: 40rem;
  }
  .search-container__header {
    font-size: 2.5rem;
  }
}
</style>
