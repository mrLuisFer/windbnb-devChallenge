<script lang="typescript">
  import { getContext } from 'svelte'
  import type { Data } from '../../types/data'
  import Card from './Card.svelte'

  export let stays: Array<Data>
  console.log(stays)

  // const inputCity: string = 'Helsinki'
  let inputCity: string = ''
  let inputContext: string = getContext('cityInputValue')

  if (inputContext !== undefined) {
    inputCity = inputContext
  }

  console.log(inputCity)
  const staysFiltered = stays.filter((city: Data) => city.city === inputCity)

  console.log(staysFiltered)
</script>

<div class="cards-layout">
  {#each stays as room}
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
