<script>
  import '../app.css';

  export let author = '';
</script>

<blockquote
  class="text-center p-4 my-4 border-s-4 border-gray-300 bg-gray-50 dark:border-gray-500 dark:bg-gray-800 rounded shadow"
>
  <p class="text-xl italic font-medium leading-relaxed text-gray-900 dark:text-white"><slot /></p>
  {#if author != ''}
    <div class="pe-3 font-medium text-gray-900 dark:text-white">{author}</div>
  {/if}
</blockquote>
