<script>
  import '../app.css';

  export let data;
</script>

<header
  class="bg-black text-white dark:bg-gray-300 dark:text-black sticky top-0 border-solid border-blue-400 border-b-4"
>
  <nav class="flex mx-auto items-center justify-between p-4">
    <a class="flex content-center" href="https://ooako.co.za">
      <abbr class="no-underline text-3xl bold pr-2" title="One Of A Kind Original">OOAKO</abbr>
      <img class="h-8" src="logo-blue.jpg" alt="One Of A Kind Original" />
    </a>
    <ul
      class="flex flex-wrap items-center justify-between space-x-3 rtl:space-x-reverse list-none p-0"
    >
      {#each data.nav as nav}
        <li class="inline m-2">
          <a class="transition-colors hover:text-blue-400 dark:hover:text-blue-800" href={nav[1]}
            >{nav[0]}</a
          >
        </li>
      {/each}
    </ul>
  </nav>
</header>
<main class="min-h-screen">
  <slot />
</main>
<footer
  class="text-center w-screen text-white bg-black py-2 border-solid border-t-4 border-blue-400"
>
  <div id="socials" class="inline-flex">
    {#each data.socials as social}
      <div class="social {social.slug} p-3">
        <a href={social.href} target="_blank"
          ><img
            alt={social.name}
            height="32"
            width="32"
            src="https://cdn.jsdelivr.net/npm/simple-icons@v11/icons/{social.slug}.svg"
          /></a
        >
      </div>
    {/each}
  </div>
  <div class="" id="footer-links"></div>
  <div id="dev-info" class="text-gray-400">
    <p>
      Created/Maintained by <a class="transition-all hover:font-bold" href="https://tagnumelite.com"
        >Tagan Hoyle</a
      >. Powered by
      <a href="https://kit.svelte.dev/">SvelteKit</a>
      using <a href="https://pages.cloudflare.com/">Cloudfare Pages</a>.
    </p>
  </div>
</footer>

<style lang="scss">
  .social {
    img {
      transition: filter 0.4s ease-in-out;
      filter: invert(99%) sepia(6%) saturate(571%) hue-rotate(222deg) brightness(119%)
        contrast(100%);
    }

    a:hover img {
      filter: invert(65%) sepia(68%) saturate(3793%) hue-rotate(136deg) brightness(107%)
        contrast(101%);
    }

    &.pinterest a:hover img {
      filter: invert(14%) sepia(98%) saturate(4590%) hue-rotate(351deg) brightness(87%)
        contrast(97%);
    }

    &.facebook a:hover img {
      filter: invert(35%) sepia(49%) saturate(3706%) hue-rotate(202deg) brightness(98%)
        contrast(94%);
    }

    &.instagram a:hover img {
      filter: invert(29%) sepia(22%) saturate(4992%) hue-rotate(295deg) brightness(95%)
        contrast(90%);
    }
  }

  #dev-info {
    a {
      text-decoration: none;
      color: #444444;

      &:hover {
        color: #b1b1b1;
      }
    }
  }
  /*
	header {
		left: 0;
		right: 0;
		text-align: center;
		color: #fff;
		background-color: #000;

		a {
			color: #fff;
			padding: 14px 16px;
			text-decoration: none;

			&:hover {
				color: #f0f;
			}
		}

		#logo {
			float: left;
			padding: 12px 16px;
			font-size: 2.5rem;
			margin-left: 3rem;
		}

		.navbar {
			float: right;
			height: 100%;
		}
	}*/
</style>
