<script>
    import Heading from "$lib/components/Heading.svelte"

    const projects = [
        {
            name: "Raga",
            desc: "A libre music frontend powered by SvelteKit.",
            link: "https://raga.vkdbois.xyz"
        },
        {
            name: "TheoOS",
            desc: "An OS-like thingy powered by SvelteKit.",
            link: "https://os.vkdbois.xyz"
        },
        {
            name: "stition.ai",
            desc: "Homepage of stition.ai.",
            link: "https://stition.ai"
        },
        {
            name: "vettucaudchurch.com",
            desc: "Website of Madre de Deus Church, Vettucaud.",
            link: "https://vettucaudchurch.com"
        },
        {
            name: "LentenRose",
            desc: "A dark theme for SDDM, made with QML.",
            link: "https://github.com/TheoIsDumb/LentenRose"
        },
        {
            name: "charapara",
            desc: "Malayali Dev Stickers!",
            link: "https://charapara.vercel.app"
        },
        {
            name: "CopyOptimize",
            desc: "An Inkscape Extension that lets you copy optimized SVGs directly from Inkscape, without having to save first.",
            link: "https://github.com/TheoIsDumb/CopyOptimize"
        }

    ]
</script>

<Heading title="Projects" />

<div class="grid md:grid-cols-2 gap-2 mt-4">
    {#each projects as proj}
        <div class="card rounded-lg bg-neutral-900 shadow-md">
            <img src="/projects/{proj.name.toLowerCase()}.webp"
            class="rounded-t-md"
            alt="Screenshot of {proj.name}">

            <div class="inside p-2 flex flex-col gap-2">
                <h4 class="text-xl font-bold text-neutral-200">{proj.name}</h4>

                <p>{proj.desc}</p>

                <a href={proj.link} target="_blank"
                class="bg-blue-600 p-2 w-fit rounded-md font-bold hover:bg-blue-500 transition duration-300"
                rel="noopener noreferrer" title={proj.name}>
                Go!
                </a>
            </div>
        </div>
    {/each}
</div>