<script>
  import Heading from "$lib/components/Heading.svelte";

  const links = [
    {
      title: "GitHub",
      link: "https://github.com/theoisdumb",
    },
    {
      title: "Art",
      link: "https://theooo.codeberg.page/",
    },
    {
      title: "Instagram (I only use it to dump my latest art)",
      link: "https://instagram.com/obpleinnds",
    },
  ];
</script>

<div class="space-y-4">
  <Heading title="About" />

  <p>Hi, I am Theo and I build stuff.</p>

  <p>
    I dabble with Svelte and JS on an almost daily basis. And I like drawing
    stuff. I mostly use
    <a href="https://inkscape.org" target="_blank">Inkscape</a>,
    <a href="https://krita.org" target="_blank">Krita</a>
    and occasionally
    <a href="https://www.blender.org/" target="_blank">Blender</a>.
  </p>

  <h2 class="font-bold text-xl">Links</h2>

  <ul class="list-inside list-disc">
    {#each links as link}
      <li>
        <a href={link.link} target="_blank">{link.title}</a>
      </li>
    {/each}
  </ul>
</div>

<style>
  a {
    @apply underline;
  }
</style>
