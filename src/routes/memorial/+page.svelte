<script>
  import Container from '$lib/Container.svelte';
  import Gallery from '$lib/Gallery.svelte';
  import Jumbotron from '$lib/Jumbotron.svelte';
  import YouTubeEmbed from '$lib/YoutubeEmbed.svelte';

  let pics = [
    { url: 'memorial/ashes.jpg', name: 'Ashes' },
    { url: 'memorial/entry-table.jpg', name: 'Entry Table' },
    { url: 'memorial/fireplace.jpg', name: 'Fireplace' },
    { url: 'memorial/looking-outside.jpg', name: 'Looking Outside' },
    { url: 'memorial/outside-brenton.jpg', name: 'Looking Outside' },
    { url: 'memorial/outside-ocena.jpg', name: 'Looking Outside' },
    { url: 'memorial/outside-pano.jpg', name: 'Looking Pano', width: 2 },
    { url: 'memorial/poster.jpg', name: 'Looking Pano' },
    { url: 'memorial/stand-left-close.jpg', name: 'Looking Pano' },
    { url: 'memorial/stand-left.jpg', name: 'Looking Pano' },
    { url: 'memorial/stand-center.jpg', name: 'Looking Pano' },
    { url: 'memorial/stand-right-close.jpg', name: 'Looking Pano' },
    { url: 'memorial/stand-right.jpg', name: 'Looking Pano' },
    { url: 'memorial/stand.jpg', name: 'Looking Pano' }
  ];
</script>

<Jumbotron img="/memorial/stand.jpg" title="Linda Hoyle's Memorial">
  <h1>Linda Hoyle's Memorial</h1>
  <p>A celebration of a life well lived.</p>
</Jumbotron>
<Container>
  <div class="min-h-dvh w-4/5 mx-auto">
    <div class="text-4xl pt-2 pb-4 text-center">
      <h1>Linda Hoyle's Memorial Livestream VOD (17-04-2024)</h1>
    </div>
    <div class="p-1 bg-black mx-3 rounded-md">
      <YouTubeEmbed url="https://www.youtube-nocookie.com/embed/WTRzrZ46TR0?si=Bc0SkmgMBGiOl8xa" />
    </div>
  </div>
</Container>
<Container>
  <Gallery pictures={pics} />
</Container>
