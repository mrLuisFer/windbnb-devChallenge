<script lang="typescript">
</script>

<div class="inputs">
  <div>
    <label for="input-location">Location</label>
    <input
      type="text"
      class="inputs-location"
      id="input-location"
      name="input-location"
      placeholder="Add location" />
  </div>
  <div>
    <label for="input-guests">Guests</label>
    <input
      type="text"
      class="inputs-guests"
      id="input-guests"
      name="input-guests"
      placeholder="Add guests" />
  </div>
</div>

<style type="text/scss" lang="scss" scoped>
  .inputs {
    border-radius: var(--border-radius);
    box-shadow: var(--default-shadow);
    height: 115px;
    margin-top: 16px;
    width: 351px;

    input {
      border: none;
      font-size: 14px;
      margin: 0;
      outline: none;
      padding: 0;

      &::placeholder {
        color: #bdbdbd;
      }
    }

    div {
      &:nth-child(1) {
        border-bottom: 1px solid #f2f2f2;
      }

      padding: 11px 26px;

      label {
        font-size: 10px;
        font-style: normal;
        font-weight: 600;
        line-height: 11px;
        margin-bottom: 5px;
        text-transform: uppercase;
      }
    }
  }
</style>
