<script lang="typescript">
  import Header from '../components/Header.svelte'
  import Searchbar from '../components/Searchbar.svelte'
  import Content from '../components/Content.svelte'
  import SearchMenu from '../components/SearchMenu/SearchMenu.svelte'

  let showMenu = false
</script>

<SearchMenu showMenu="{showMenu}" />
<div>
  <Header />
  <div class="searchbar-toHide">
    <Searchbar />
  </div>
</div>
<Content />

<style type="text/scss" lang="scss">
  .searchbar-toHide {
    @media (min-width: 1024px) {
      display: none;
    }
  }
</style>
