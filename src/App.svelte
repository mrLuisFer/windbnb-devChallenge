<script>
  import Header from './components/Header.svelte'
  import Searchbar from './components/Searchbar.svelte'
  import Content from './components/Content.svelte'
</script>

<main class="container">
  <Header />
  <Searchbar />
  <Content />
</main>

<style type="text/scss" lang="scss">
  .container {
    display: block;
  }
</style>
