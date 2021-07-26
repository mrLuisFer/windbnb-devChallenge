<script>
</script>

<div class="searchbar">
  <input
    type="text"
    class="searchbar-input searchbar-input-city"
    placeholder="Search city" />
  <input
    type="text"
    class="searchbar-input searchbar-input-guests"
    placeholder="Add guests" />
  <div class="searchbar-search-btn">
    <span class="material-icons searchbar-search-icon"> search </span>
  </div>
</div>

<style type="text/scss" lang="scss" scoped>
  .searchbar {
    align-items: center;
    border-radius: var(--border-radius);
    box-shadow: var(--default-shadow);
    display: flex;
    height: 55px;
    margin: 0 auto;
    position: relative;
    width: 300px;

    @media (min-width: 768px) {
      width: 450px;
    }

    @media (min-width: 1024px) {
      width: 300px;
    }

    &-input {
      border: none;
      border-right: 1.5px solid rgba(242, 242, 242, 1);
      font-size: 14px;
      font-weight: 400;
      height: 100%;
      outline: none;
      padding-left: 12px;
      margin-bottom: -0.8px;
      border-radius: var(--border-radius) 0 0 var(--border-radius);

      &-city {
        width: 128px;

        @media (min-width: 768px) {
          width: 208px;
        }

        @media (min-width: 1024px) {
          width: 128px;
        }
      }
      &-guests {
        width: 106px;

        @media (min-width: 768px) {
          width: 176px;
        }

        @media (min-width: 1024px) {
          width: 106px;
        }
      }
    }

    &-search {
      &-btn {
        align-items: center;
        border-radius: 0 var(--border-radius) var(--border-radius) 0;
        cursor: pointer;
        display: flex;
        height: 100%;
        justify-content: center;
        position: relative;
        transition: var(--transition);
        width: 100%;

        &:hover {
          background: var(--primary-red);

          & > span {
            color: #eee;
          }
        }
      }

      &-icon {
        color: var(--primary-red);
      }
    }
  }
</style>
