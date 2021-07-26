<script>
  import CardsLayout from './CardsLayout/CardsLayout.svelte'
</script>

<section class="content">
  <div class="content-header">
    <h1 class="content-title">Stays in Finland</h1>
    <p class="content-stays">12+ stays</p>
  </div>
  <CardsLayout />
</section>

<style type="text/scss" lang="scss">
  .content {
    padding: var(--mobile-padding);
    margin-top: 37px;

    &-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    &-title {
      font-weight: 700;
      font-size: 1.1rem;
      letter-spacing: 0.5px;
    }

    &-stays {
      font-size: 14px;
      font-weight: 500;
      color: var(--secondary-text-color);
    }
  }
</style>
