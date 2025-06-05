<script>
  import '../app.css';

  //export let spacing = 2;
</script>

<div class="cgrid flex flex-wrap items-stretch mx-auto justify-between p-4 gap-6">
  <slot />
</div>

<style lang="scss">
  .cgrid :global(*) {
    flex: 1 0 21%;
  }
</style>