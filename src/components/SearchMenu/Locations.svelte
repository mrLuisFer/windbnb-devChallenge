<script lang="typescript">
  import { stays } from '../../api/stays'
  import type { Data } from '../../types/data'

  const cities: string[] = stays.map((city: Data) => city.city)

  const citiesFiltered = stays.filter(
    ({ city }: Data, index: number) => !cities.includes(city, index + 1)
  )
  console.log(citiesFiltered)
</script>

<div class="locations">
  {#each citiesFiltered as city}
    <div class="locations-content">
      <span class="material-icons"> place </span>
      <p>
        {city.city}, {city.country}
      </p>
    </div>
  {/each}
</div>

<style type="text/scss" lang="scss">
  .locations {
    margin-top: 35px;
    padding: 0 var(--mobile-padding);

    &-content {
      align-items: center;
      color: #4f4f4f;
      column-gap: 5px;
      display: flex;
      margin-bottom: 24px;

      p {
        font-size: 14px;
        font-weight: normal;
        line-height: 18px;
      }
    }
  }
</style>
