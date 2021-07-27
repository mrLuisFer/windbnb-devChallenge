<script lang="typescript">
  import Header from '../components/Header.svelte'
  import Searchbar from '../components/Searchbar.svelte'
  import Content from '../components/Content.svelte'
  import SearchMenu from '../components/SearchMenu/SearchMenu.svelte'

  let showMenu = false
</script>

<SearchMenu showMenu="{showMenu}" />
<div class="layout">
  <Header />
  <div class="searchbar-toHide">
    <Searchbar />
  </div>
  <Content />
</div>

<style type="text/scss" lang="scss">
  .searchbar-toHide {
    @media (min-width: 1024px) {
      display: none;
    }
  }

  .layout {
    @media (min-width: 768px) {
      padding: var(--tablet-padding);
    }

    @media (min-width: 1024px) {
      max-width: 1250px;
      position: relative;
      margin: 0 auto;
    }
  }
</style>
