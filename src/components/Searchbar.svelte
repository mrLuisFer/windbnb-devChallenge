<script>
</script>

<div class="searchbar">
  <div class="searchbar-content flex-center">
    <p class="searchbar-content-text">Helsinski, Finland</p>
  </div>
  <div class="searchbar-content flex-center">
    <p class="searchbar-content-text">Add Guests</p>
  </div>
  <div class="searchbar-search flex-center">
    <span class="material-icons searchbar-search-icon"> search </span>
  </div>
</div>

<style type="text/scss" lang="scss" scoped>
  .flex-center {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .searchbar {
    align-items: center;
    border-radius: var(--border-radius);
    box-shadow: var(--default-shadow);
    display: flex;
    font-size: 14px;
    height: 55px;
    justify-content: space-between;
    margin: 0 auto;
    position: relative;
    width: 300px;

    &-content {
      border-right: 1.5px solid rgba(242, 242, 242, 1);
      height: 100%;
      padding: 0 14px;

      &-text {
        margin: 0;
      }
    }
    &-search {
      width: 36px;

      &-icon {
        color: var(--primary-red);
        font-weight: 500;
        cursor: pointer;
      }
    }
  }
</style>
