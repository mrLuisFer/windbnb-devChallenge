<script lang="ts">
  import { stays } from '../../api/stays'
  import Card from './Card.svelte'

  console.log(stays)
</script>

<div class="cards-layout">
  {#each stays as room}
    <Card data="{room}" />
  {/each}
</div>

<style type="text/scss" lang="scss">
</style>
