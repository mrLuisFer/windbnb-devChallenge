<script lang="ts">
  import type { Data } from '../../types/data'

  export let data: Data

  const {
    beds,
    city,
    country,
    maxGuests,
    photo,
    rating,
    superHost,
    title,
    type
  } = data
</script>

<div class="card">
  <img
    class="card-img"
    src="{photo}"
    alt="{title}"
    title="{title}"
    loading="lazy" />
  <div class="card-details">
    {#if superHost}
      <p>super host</p>
    {/if}
  </div>
</div>

<style type="text/scss" lang="scss">
  .card {
    &-img {
      width: 350px;
      height: 238px;
      border-radius: var(--border-radius);
    }
  }
</style>
