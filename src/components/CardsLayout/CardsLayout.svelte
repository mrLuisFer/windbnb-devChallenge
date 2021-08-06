<script lang="typescript">
  import { getContext } from 'svelte'
  import type { Data } from '../../types/data'
  import Card from './Card.svelte'

  export let stays: Array<Data>

  // const inputCity: string = 'Helsinki'
  let inputCity: string = ''
  console.log(inputCity)

  let staysFiltered = stays.filter(
    ({ city }: Data) => city.indexOf(inputCity) !== -1
  )

  console.log(staysFiltered)
</script>

<div class="cards-layout">
  {#each staysFiltered as room}
    <Card data="{room}" />
  {/each}
</div>

<style type="text/scss" lang="scss">
  .cards-layout {
    @media (min-width: 750px) {
      display: flex;
      flex-wrap: wrap;
      gap: 40px;
      justify-content: space-around;
      align-items: center;
    }
  }
</style>
