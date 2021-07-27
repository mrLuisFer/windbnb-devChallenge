<script lang="typescript">
  import Searchbar from './Searchbar.svelte'
</script>

<header class="header">
  <img
    src="/images/logo.svg"
    alt="DevChallenges"
    class="header-logo"
    draggable="false" />

  <div class="header-searchbar">
    <Searchbar />
  </div>
</header>

<style type="text/scss" lang="scss">
  .header {
    padding: var(--mobile-padding);
    display: flex;
    justify-content: space-between;

    &-logo {
      @media (min-width: 768px) {
        width: 100px;
        height: 20px;
      }

      @media (min-width: 1024px) {
        height: auto;
        margin: auto 0;
      }
    }

    &-searchbar {
      display: none;

      @media (min-width: 1024px) {
        display: block;
      }
    }
  }
</style>
