<script lang="ts">
  import type { Data } from '../../types/data'
  import Card from './Card.svelte'
  export let stays: Array<Data>

  console.log(stays)
</script>

<div class="cards-layout">
  {#each stays as room}
    <Card data="{room}" />
  {/each}
</div>

<style type="text/scss" lang="scss">
  .cards-layout {
    display: flex;
    flex-wrap: wrap;
    gap: 40px;
    justify-content: space-around;
    align-items: center;
  }
</style>
