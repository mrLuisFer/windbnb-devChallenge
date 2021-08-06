<script lang="typescript">
  import type { Data } from '../../types/data'

  export let data: Data

  const { city, beds, photo, rating, superHost, title, type } = data
</script>

<article class="card">
  <img
    class="card-img"
    src="{photo}"
    alt="{title}"
    title="{city} - {title}"
    loading="lazy" />
  <div class="card-details">
    <div class="card-details-content">
      {#if superHost}
        <div class="card-details-superhost"><p>super host</p></div>
      {/if}
      {#if type.length > 0}
        <p class="card-details-type">
          {type}
          {beds >= 2 ? `. ${beds} beds` : ''}
        </p>
      {/if}
    </div>
    <p class="card-rating">
      <span class="material-icons card-rating-star-icon" title="{rating} Stars">
        star_rate
      </span>
      {rating}
    </p>
  </div>
  <p class="card-title">{title}</p>
</article>

<style type="text/scss" lang="scss">
  .card {
    margin: 35px auto;
    display: block;
    max-width: 350px;

    @media (min-width: 750px) {
      width: 300px;
      margin: 35px 0;
    }

    @media (min-width: 1020px) {
      width: 350px;
    }

    &-img {
      border-radius: var(--border-radius);
      height: 238px;
      width: 350px;
      margin-bottom: 13px;
      object-fit: cover;

      @media (min-width: 750px) {
        width: 300px;
      }

      @media (min-width: 1020px) {
        width: 350px;
        height: 250px;
      }
    }

    &-details {
      align-items: center;
      display: flex;
      justify-content: space-between;

      &-content {
        display: flex;
        align-items: center;
        column-gap: 11px;
      }

      &-superhost {
        align-items: center;
        border-radius: 12px;
        border: 1px solid var(--secondary-text-color);
        color: var(--secondary-text-color);
        display: inline-flex;
        font-size: 10px;
        font-weight: 600;
        height: 25px;
        padding: 7px;
        text-align: center;
        text-transform: uppercase;
        transition: var(--transition);

        &:hover {
          background: var(--secondary-text-color);
          color: #fff;
        }

        p {
          margin: 0;
          line-height: 1px;
          font-weight: 600;
        }
      }

      &-type {
        color: var(--text-gray);
        font-weight: 400;
        font-size: 12px;
      }
    }

    &-rating {
      align-items: center;
      display: flex;
      font-size: 12px;
      color: var(--secondary-text-color);
      font-weight: 500;

      &-star-icon {
        color: var(--primary-red);
        margin-right: 4px;
        transition: var(--transition);

        &:hover {
          filter: brightness(1.3);
        }
      }
    }

    &-title {
      font-size: 14px;
      margin-top: 10px;
      font-weight: 600;
    }
  }
</style>
