<script lang="typescript">
  import Searchbar from './Searchbar.svelte'
</script>

<header class="header">
  <img src="/images/logo.svg" alt="DevChallenges" />

  <div class="header-searchbar">
    <Searchbar />
  </div>
</header>

<style type="text/scss" lang="scss">
  .header {
    padding: var(--mobile-padding);
    display: flex;
    justify-content: space-between;

    &-searchbar {
      display: none;

      @media (min-width: 1024px) {
        display: block;
      }
    }
  }
</style>
