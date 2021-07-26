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
    <div class="card-details-content">
      {#if superHost}
        <div class="card-details-superhost"><p>super host</p></div>
      {/if}
      {#if type.length > 0}
        <p class="card-details-type">{type}</p>
      {/if}
    </div>
    <p class="card-rating">
      <span class="material-icons card-rating-star-icon"> star_rate </span>
      {rating}
    </p>
  </div>
</div>

<style type="text/scss" lang="scss">
  .card {
    margin: 32px 0;

    &-img {
      border-radius: var(--border-radius);
      height: 238px;
      width: 350px;
    }

    &-details {
      align-items: center;
      display: flex;
      justify-content: space-between;

      &-content {
        display: flex;
      }

      &-superhost {
        align-items: center;
        border-radius: 12px;
        border: 1px solid var(--secondary-text-color);
        color: var(--secondary-text-color);
        display: inline-flex;
        font-size: 0.8rem;
        font-weight: 600;
        height: 25px;
        padding: 7px;
        text-align: center;
        text-transform: uppercase;

        p {
          margin: 0;
          line-height: 1px;
        }
      }

      &-type {
        color: var(--text-gray);
        font-weight: 400;
        font-size: 14px;
      }
    }

    &-rating {
      align-items: center;
      display: flex;
      font-size: 12px;
      color: var(--secondary-text-color);

      &-star-icon {
        color: var(--primary-red);
      }
    }
  }
</style>
