<script>
  import '../app.css';

  /** @type string? */
  export let img;
  /** @type string */
  export let title;
  /** @type string? */
  export let subtitle = null;
</script>

<div class="container bg-center md:bg-right-top" style="background-image: url({img})">
  <div class="jumbotron">
    <div class="title">
      <p>{title}</p>
      {#if subtitle}
        <p class="subtitle">{subtitle}</p>
      {/if}
    </div>
    <div class="info">
      <slot />
    </div>
  </div>
</div>

<style lang="scss">
  .container {
    width: 100%;
    background-size: 100vw;
    border-bottom: 2px solid #000;
    background-repeat: no-repeat;
    background-position: top;

    .jumbotron {
      padding: 7rem 3rem;
      color: #e4e4e4;
      text-align: center;
      text-shadow: 2px 2px #000;
      margin-left: auto;
      margin-right: auto;

      .title {
        font-size: 4rem;
        &:first-child p {
          margin-bottom: 0;
        }

        .subtitle {
          font-size: 1.5rem;
          margin-top: 0;
        }
      }

      .info {
        margin-top: 1rem;

        :global(p) {
          font-size: 1.2rem;
          text-shadow: 0.1em 0.1em #000;
        }
      }
    }
  }
</style>
