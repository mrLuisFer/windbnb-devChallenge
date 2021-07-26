<script>
  import Header from './components/Header.svelte'
  import Searchbar from './components/Searchbar.svelte'
  import Content from './components/Content.svelte'
  import SearchMenu from './components/SearchMenu/SearchMenu.svelte'
</script>

<main class="container">
  <SearchMenu />
  <div>
    <Header />
    <div class="searchbar-toHide">
      <Searchbar />
    </div>
  </div>
  <Content />
</main>

<style type="text/scss" lang="scss">
  .container {
    display: block;
  }

  .searchbar-toHide {
    @media (min-width: 1024px) {
      display: none;
    }
  }
</style>
