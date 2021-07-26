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
  <img src="{photo}" alt="{title}" title="{title}" />
</div>

<style type="text/scss" lang="scss">
</style>
