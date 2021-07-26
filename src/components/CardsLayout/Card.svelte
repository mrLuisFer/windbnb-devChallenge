<script>
  export let data

  const {
    city,
    country,
    superHost,
    title,
    rating,
    maxGuests,
    type,
    beds,
    photo
  } = data
</script>

<div class="card">
  <img src="{photo}" alt="{title}" title="{title}" />
</div>

<style type="text/scss" lang="scss">
</style>
