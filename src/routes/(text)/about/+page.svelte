<script>
  import Heading from "$lib/components/Heading.svelte";
  import { icons } from "$lib/icons";

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

  <p>Hi, I am Theo and I like customizing stuff.</p>

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

  <h2 class="font-bold text-xl">Tools I Use</h2>

  <div class="flex flex-wrap gap-4">
    {#each icons as icon}
      <div class="flex flex-col gap-2 items-center">
        <span class="hover:scale-110">{@html icon.svg}</span>
        <span class="font-bold text-xs">{icon.title}</span>
      </div>
    {/each}
  </div>
</div>

<style>
  a {
    @apply underline;
  }
  :global(svg.icon) {
    @apply size-10;
  }
</style>
