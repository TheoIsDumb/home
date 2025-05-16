<script>
  import Heading from "$lib/components/Heading.svelte";

  const projects = [
    {
      name: "Home",
      desc: "This website. Made with Threlte.",
      link: "https://home.vkdbois.xyz",
      github: "https://github.com/TheoIsDumb/home",
    },
    {
      name: "Raga",
      desc: "[INACTIVE] A libre music frontend powered by SvelteKit.",
      link: "https://raga.vkdbois.xyz",
      github: "https://github.com/TheoIsDumb/raga",
    },
    {
      name: "TheoOS",
      desc: "An OS-like thingy powered by SvelteKit.",
      link: "https://os.vkdbois.xyz",
      github: "https://github.com/TheoIsDumb/TheoOS",
    },
    {
      name: "Funkwest",
      desc: "A font I made for fun.",
      link: "https://funkwest-web.vercel.app",
      github: "https://github.com/TheoIsDumb/funkwest",
    },
    {
      name: "Codex",
      desc: "A system info utility for Linux.",
      github: "https://github.com/TheoIsDumb/codex",
    },
    {
      name: "launch2",
      desc: "A theme for the Bridge Android Launcher, made with web technologies..",
      github: "https://github.com/TheoIsDumb/launch2",
    },
    {
      name: "Halo",
      desc: "A JioSaavn frontend made with Tkinter.",
      github: "https://github.com/TheoIsDumb/halo",
    },
    {
      name: "stition.ai",
      desc: "Homepage of stition.ai.",
      link: "https://stition.ai",
    },
    {
      name: "Hypx",
      desc: "Homepage of hypx.in.",
      link: "https://hypx.in",
    },
    {
      name: "vettucaudchurch.com",
      desc: "Website of Madre de Deus Church, Vettucaud.",
      link: "https://vettucaudchurch.com",
    },
    {
      name: "LentenRose",
      desc: "A dark theme for SDDM, made with QML.",
      github: "https://github.com/TheoIsDumb/LentenRose",
    },
    {
      name: "charapara",
      desc: "Malayali Dev Stickers!",
      link: "https://charapara.vercel.app",
    },
    {
      name: "CopyOptimize",
      desc: "An Inkscape Extension that lets you copy optimized SVGs directly from Inkscape, without having to save first.",
      github: "https://github.com/TheoIsDumb/CopyOptimize",
    },
  ];
</script>

<Heading title="Projects" />

<div class="grid lg:grid-cols-2 gap-2 mt-4">
  {#each projects as proj}
    <div class="card rounded-lg bg-neutral-900 shadow-md">
      <img
        loading="lazy"
        src="/projects/{proj.name.toLowerCase()}.webp"
        class="rounded-t-md"
        alt="Screenshot of {proj.name}"
      />

      <div class="inside p-3 flex flex-col gap-4">
        <h4 class="text-xl font-bold text-neutral-200">{proj.name}</h4>

        <p>{proj.desc}</p>

        <div class="links flex gap-2">
          {#if proj.hasOwnProperty("link")}
            <a
              href={proj.link}
              target="_blank"
              rel="noopener noreferrer"
              title={proj.name}
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="32"
                height="32"
                viewBox="0 0 256 256"
                ><path
                  fill="currentColor"
                  d="M128 24a104 104 0 1 0 104 104A104.12 104.12 0 0 0 128 24m88 104a87.6 87.6 0 0 1-3.33 24h-38.51a157.4 157.4 0 0 0 0-48h38.51a87.6 87.6 0 0 1 3.33 24m-114 40h52a115.1 115.1 0 0 1-26 45a115.3 115.3 0 0 1-26-45m-3.9-16a140.8 140.8 0 0 1 0-48h59.88a140.8 140.8 0 0 1 0 48ZM40 128a87.6 87.6 0 0 1 3.33-24h38.51a157.4 157.4 0 0 0 0 48H43.33A87.6 87.6 0 0 1 40 128m114-40h-52a115.1 115.1 0 0 1 26-45a115.3 115.3 0 0 1 26 45m52.33 0h-35.62a135.3 135.3 0 0 0-22.3-45.6A88.29 88.29 0 0 1 206.37 88Zm-98.74-45.6A135.3 135.3 0 0 0 85.29 88H49.63a88.29 88.29 0 0 1 57.96-45.6M49.63 168h35.66a135.3 135.3 0 0 0 22.3 45.6A88.29 88.29 0 0 1 49.63 168m98.78 45.6a135.3 135.3 0 0 0 22.3-45.6h35.66a88.29 88.29 0 0 1-57.96 45.6"
                /></svg
              >
            </a>
          {/if}

          {#if proj.hasOwnProperty("github")}
            <a
              href={proj.github}
              target="_blank"
              rel="noopener noreferrer"
              title={proj.name}
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="32"
                height="32"
                viewBox="0 0 24 24"
                ><path
                  fill="currentColor"
                  d="M12 2A10 10 0 0 0 2 12c0 4.42 2.87 8.17 6.84 9.5c.5.08.66-.23.66-.5v-1.69c-2.77.6-3.36-1.34-3.36-1.34c-.46-1.16-1.11-1.47-1.11-1.47c-.91-.62.07-.6.07-.6c1 .07 1.53 1.03 1.53 1.03c.87 1.52 2.34 1.07 2.91.83c.09-.65.35-1.09.63-1.34c-2.22-.25-4.55-1.11-4.55-4.92c0-1.11.38-2 1.03-2.71c-.1-.25-.45-1.29.1-2.64c0 0 .84-.27 2.75 1.02c.79-.22 1.65-.33 2.5-.33s1.71.11 2.5.33c1.91-1.29 2.75-1.02 2.75-1.02c.55 1.35.2 2.39.1 2.64c.65.71 1.03 1.6 1.03 2.71c0 3.82-2.34 4.66-4.57 4.91c.36.31.69.92.69 1.85V21c0 .27.16.59.67.5C19.14 20.16 22 16.42 22 12A10 10 0 0 0 12 2"
                /></svg
              >
            </a>
          {/if}
        </div>
      </div>
    </div>
  {/each}
</div>

<style>
  svg {
    transition: all 300ms;
  }
  svg:hover {
    filter: drop-shadow(0 0 0.3rem white);
  }
</style>
