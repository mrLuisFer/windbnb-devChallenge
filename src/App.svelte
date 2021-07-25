<script>
  import Header from './components/Header.svelte'
  import Searchbar from './components/Search.svelte'
</script>

<main class="container">
  <Header />
  <Searchbar />
  <h1>Hello!</h1>
</main>

<style type="text/scss" lang="scss">
  @import './scss/normalize.scss';

  .container {
    display: block;
  }
</style>
