<script lang="typescript">
  import { getContext } from 'svelte'
  import Inputs from './Inputs.svelte'
  import Locations from './Locations.svelte'
  import Button from './Button.svelte'

  let { value } = getContext('showMenu')

  const menuClass = !value && 'hidde'

  const closeMenu = () => {
    console.log('closing')
    value = false
    console.log(value)
  }
</script>

<div class="searchMenu {menuClass}">
  <div class="searchMenu-header">
    <p class="searchMenu-header-text">Edit your search</p>
    <span class="material-icons" on:click="{closeMenu}"> close </span>
  </div>
  <Inputs />
  <Locations />
  <Button />
</div>

<style type="text/scss" lang="scss">
  .searchMenu {
    position: fixed;
    background: #fff;
    padding: var(--mobile-padding);
    width: 100%;
    z-index: 99;
    /* height: 632px; */

    &-header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      color: var(--primary-text-color);

      &-text {
        font-size: 12px;
        line-height: 15px;
        font-weight: 600;
      }
    }
  }

  .hidde {
    display: none;
  }
</style>
