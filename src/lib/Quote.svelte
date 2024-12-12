<script>
  import '../app.css';

  export let author = '';
</script>

<blockquote>
	<p><slot /></p>
  {#if author != ''}
    <div class="pe-3 font-medium text-gray-900 dark:text-white">{author}</div>
  {/if}
</blockquote>

<style lang="scss">
	blockquote {
		margin: 1.5rem auto;
		max-width: 60vw;
		text-align: center;
		background-color: #e7e7e7;
		padding: 1rem;
		border-radius: 1rem;

		footer {
			color: rgb(124, 124, 124);

			&::before {
				color: black;
				content: '— ';
			}
		}
	}
</style>
