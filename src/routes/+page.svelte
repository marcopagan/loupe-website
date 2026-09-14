<script>
	import FeaturesSection from '$lib/components/FeaturesSection.svelte';
	import Hero from '$lib/components/Hero.svelte';
    import TopNav from '$lib/components/TopNav.svelte';
	import { IconArrowUpRight, IconMailFast } from '@tabler/icons-svelte';
    import { base } from '$app/paths';
</script>



<TopNav />

<main class="grid grid-cols-1 my-0 lg:my-16">
    


    <Hero />


    <!-- What is it (with border) -->
    <section class="container mx-auto grid grid-cols-12 gap-16 py-24 lg:py-48 px-16">
        <div class="col-span-12 lg:col-span-5 flex justify-center flex-col gap-16 lg:pr-48">
            <h2 class="h2">What is it?</h2>
            <p class="text-surface-600">
                Loupe is a platform for provenance research. Structure an object's ownership history event by event, link each step to its supporting evidence, and visualize the full timeline, turning scattered archival research into a clear, shareable record.
            </p>
        </div>
        <div class="col-span-12 lg:col-span-7 bg-primary-500 lg:p-48 flex flex-wrap items-center justify-center rounded-lg">
            <iframe class="rounded-lg lg:rounded-xl shadow-xl aspect-video w-full h-auto" width="853" height="480" src="https://www.youtube-nocookie.com/embed/LXb3EKWsInQ?si=9aYDBlmUxg4YmG-a" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
        </div>
    </section>






    <!-- Feature -->
    <FeaturesSection />






    <!-- About colored background (center) -->
    <section class="py-24 lg:py-120 bg-primary-100">
        <div class="container mx-auto gap-32 lg:gap-48 px-16 py-16 lg:py-0 flex flex-col flex-wrap items-center">
        <div class="flex justify-center flex-col gap-16 lg:w-lg text-center">
            <h2 class="h2">About the project</h2>
            <p class="text-surface-600 text-balance">
                Vivamus eget consequat justo. Quisque hendrerit augue eu dignissim bibendum. Fusce ut est sed nibh bibendum auctor in et urna. Praesent et tincidunt elit.
            </p>
        </div>
        <div class="col-span-12 lg:col-span-7 flex flex-col md:flex-row gap-16">
            <div class="card p-16 preset-outlined flex flex-col gap-16 bg-neutral-50" style="border: 1.5px solid var(--color-surface-200)">
                <div class="flex flex-wrap items-center gap-16">
                    <img src={`${base}/imgs/card-db.svg`} width="48" height="48" alt="Digital Benin logo">
                    <h3 class="h3">Digital Benin</h3>
                </div>
                <p class="text-sm" style="height: stretch">Digital Benin brings together all objects, historical photographs and rich documentation material from collections worldwide to provide a long-requested overview of the royal artefacts from Benin Kingdom looted in the late nineteenth century. </p>
                <a href="https://digitalbenin.org" target="_blank" rel="noopener" class="btn preset-tonal-surface bg-surface-100 p-16 hover:gap-12 lg:w-3xs">
                    Go to the website
                    <IconArrowUpRight stroke="1.5" class="size-18" />
                </a>
            </div>
            <div class="card p-16 preset-outlined flex flex-col gap-16 bg-neutral-50" style="border: 1.5px solid var(--color-surface-200)">
                <div class="flex flex-wrap items-center gap-16">
                    <img src={`${base}/imgs/card-okpan.svg`} width="48" height="48" alt="Ọkpan logo">
                    <h3 class="h3">Ọkpan</h3>
                </div>
                <p class="text-sm" style="height: stretch">Ọkpan is a platform for reconnecting dispersed collections. Import artefact records from any source, enrich them with situated knowledge such as Indigenous designations, oral histories, and cultural context, and publish a unified catalogue that brings a scattered collection back together, wherever the objects themselves remain.</p>
                <a href="https://digitalbenin.org" target="_blank" rel="noopener" class="btn preset-tonal-surface bg-surface-100 p-16 hover:gap-12 lg:w-3xs">
                    Discover it
                    <IconArrowUpRight stroke="1.5" class="size-18" />
                </a>
            </div>
        </div>
        </div>
    </section>



    <!-- About white background (side)
    <section class="container mx-auto grid grid-cols-12 gap-16 py-24 lg:py-96 px-16">
        <div class="col-span-12 lg:col-span-5 flex justify-center flex-col gap-16 lg:pr-48">
            <h2 class="h2">About the project</h2>
            <p class="text-surface-600">
                Vivamus eget consequat justo. Quisque hendrerit augue eu dignissim bibendum. Fusce ut est sed nibh bibendum auctor in et urna. Praesent et tincidunt elit.
            </p>
        </div>
        <div class="col-span-12 lg:col-span-7 flex flex-col md:flex-row gap-16">
            <div class="card p-16 preset-outlined flex flex-col gap-16" style="border: 1.5px solid var(--color-surface-100)">
                <img src={`${base}/imgs/card-db.svg`} width="48" height="48" alt="Digital Benin logo">
                <h4 class="font-semibold">Digital Benin</h4>
                <p class="text-sm" style="height: stretch">Digital Benin brings together all objects, historical photographs and rich documentation material from collections worldwide to provide a long-requested overview of the royal artefacts from Benin Kingdom looted in the late nineteenth century. </p>
                <a href="https://digitalbenin.org" target="_blank" rel="noopener" class="btn preset-tonal-brand p-16 hover:gap-12">
                    Go to the website
                    <IconArrowUpRight stroke="1.5" class="size-18" />
                </a>
            </div>
            <div class="card p-16 preset-outlined flex flex-col gap-16" style="border: 1.5px solid var(--color-surface-100)">
                <img src={`${base}/imgs/card-loupe.svg`} width="48" height="48" alt="Loupe logo">
                <h4 class="font-semibold">Loupe</h4>
                <p class="text-sm" style="height: stretch">Loupe is a platform for provenance research. Structure an object's ownership history event by event, link each step to its supporting evidence, and visualize the full timeline, turning scattered archival research into a clear, shareable record.</p>
                <a href="https://digitalbenin.org" target="_blank" rel="noopener" class="btn preset-tonal-brand p-16 hover:gap-12">
                    Discover it
                    <IconArrowUpRight stroke="1.5" class="size-18" />
                </a>
            </div>
        </div>
    </section>  -->






    <!-- Contacts (dark bg) -->
    <section class="py-24 lg:py-120 bg-primary-800">
        <div class="container mx-auto flex flex-col gap-16 px-16">
            <h2 class="h2 text-white">Contact us</h2>
            <div class="lg:columns-2 pb:24">
                <p class="text-primary-100">
                    Quisque lacus arcu, ornare eget porta id, lobortis a nulla. In tortor nisl, rhoncus sed efficitur sollicitudin, sagittis vel lacus. In quis porta neque. Ut id ante sed urna accumsan auctor. Nulla suscipit pellentesque nibh, id ultricies tortor porta quis. Vestibulum nec augue ut ex hendrerit feugiat. Phasellus ornare tortor a ullamcorper ultrices. Morbi id elementum est. Cras sodales mollis mi id vestibulum.
                    <br>
                    Integer varius eros nec pharetra tristique. Nam id dui neque. Sed varius eget urna vel dapibus. Vivamus posuere neque vel massa porta ultrices. Nunc eget ipsum at nisi eleifend rhoncus. Quisque facilisis felis vitae massa posuere, in imperdiet diam semper. Morbi vestibulum hendrerit augue ac congue. Vestibulum imperdiet nisl sed mattis commodo.
                </p>
            </div>
            <a href="https://digitalbenin.org" target="_blank" rel="noopener" class="btn preset-filled-brand text-white p-16 gap-8 hover:gap-12 lg:w-3xs">
                Send us an email
                <IconMailFast stroke="1.5" class="size-18" />
            </a>
        </div>
    </section>

    <!-- Contacts (light bg)
    <section class="py-24 lg:py-120 bg-primary-100">
        <div class="container mx-auto flex flex-col gap-16 px-16">
            <h2 class="h2">Contact us</h2>
            <div class="lg:columns-2 pb:24">
                <p class="text-primary-900">
                    Quisque lacus arcu, ornare eget porta id, lobortis a nulla. In tortor nisl, rhoncus sed efficitur sollicitudin, sagittis vel lacus. In quis porta neque. Ut id ante sed urna accumsan auctor. Nulla suscipit pellentesque nibh, id ultricies tortor porta quis. Vestibulum nec augue ut ex hendrerit feugiat. Phasellus ornare tortor a ullamcorper ultrices. Morbi id elementum est. Cras sodales mollis mi id vestibulum.
                    <br>
                    Integer varius eros nec pharetra tristique. Nam id dui neque. Sed varius eget urna vel dapibus. Vivamus posuere neque vel massa porta ultrices. Nunc eget ipsum at nisi eleifend rhoncus. Quisque facilisis felis vitae massa posuere, in imperdiet diam semper. Morbi vestibulum hendrerit augue ac congue. Vestibulum imperdiet nisl sed mattis commodo.
                </p>
            </div>
            <a href="https://digitalbenin.org" target="_blank" rel="noopener" class="btn preset-filled-brand bg-primary-600 text-white p-16 gap-8 hover:gap-12 lg:w-3xs">
                Send us an email
                <IconMailFast stroke="1.5" class="size-18" />
            </a>
        </div>
    </section> -->








    <!-- Sponsor -->
    <section class="container mx-auto flex flex-wrap gap-24 lg:gap-48 py-32 lg:py-96 px-16">

        <div class="flex flex-col pt-16 lg:pt-0 gap-16 w-full lg:w-auto">
            <p class="text-surface-600 text-sm">With the generous support of</p>
            <div class="flex flex-row flex-wrap gap-24">
                <img src={`${base}/imgs/supp-1.png`} width="106" height="80" alt="Evs" class="h-fit">
                <img src={`${base}/imgs/supp-2.png`} width="307" height="80" alt="Mellon Foundation" class="h-fit">
            </div>
        </div>

        <div class="flex flex-col pt-16 border-t-[1.5px] md:border-t-0 border-surface-200 lg:pt-0 gap-16 w-full lg:w-auto">
            <p class="text-surface-600 text-sm">Hosted by</p>
            <div class="flex flex-row flex-wrap gap-24">
                <img src={`${base}/imgs/supp-3.png`} width="201" height="80" alt="Markk" class="h-fit">
            </div>
        </div>

        <div class="flex flex-col pt-16 border-t-[1.5px] md:border-t-0 border-surface-200 lg:pt-0 gap-16 w-full lg:w-auto">
            <p class="text-surface-600 text-sm">In collaboration with</p>
            <div class="flex flex-row flex-wrap gap-24">
                <img src={`${base}/imgs/supp-4.png`} width="114" height="80" alt="Markk" class="h-fit">
                <img src={`${base}/imgs/supp-5.png`} width="56" height="80" alt="Markk" class="h-fit">
                <img src={`${base}/imgs/supp-6.png`} width="80" height="80" alt="Markk" class="h-fit">
                <img src={`${base}/imgs/supp-7.png`} width="137" height="80" alt="Markk" class="h-fit">
            </div>
        </div>
    </section>





</main>


<!-- Footer (dark) -->
<footer class="bg-linear-to-t from-black to-primary-900 py-48 px-16 relative overflow-hidden h-450 lg:h-auto">
    <div class="container mx-auto grid grid-cols-12 gap-24 z-64 relative">

        <div class="col-span-12 lg:col-span-4 flex flex-col gap-24">
            <div class="flex flex-wrap items-center gap-8">
                <img src={`${base}/brand/icon-logo.svg`} width="40" height="40" alt="Ọkpan logo">
                <h3 class="h3 text-white">Loupe</h3>
            </div>

            <p class="text-primary-200 text-balance">
                Loupe helps researchers build, visualize, and share the evidence behind an object's history, from its first known record to today.
            </p>
        </div>

        <div class="col-span-12 lg:col-span-3 lg:col-start-9 lg:flex lg:items-end lg:justify-end">
            <p class="text-primary-200 text-sm">Information in a small size</p>
        </div>

    </div>

    <img src={`${base}/brand/footer-logo.svg`} width="750" height="249" alt="Loupe footer logo" class="logo-footer absolute bottom-[-32px] md:bottom-[-64px] right-0 md:right-[5%] w-[140vw] md:w-[700px] h-auto z-32"/>
</footer>