<script lang="ts">
    import { IconArrowUpRight } from '@tabler/icons-svelte';
    import { Dialog  } from '@skeletonlabs/skeleton-svelte';
	import MobileModal from './MobileModal.svelte';
    import { base } from '$app/paths';
</script>

<section class="container mx-auto px-0 md:px-16">
    <div class="hero h-[80vh] sm:rounded-lg relative overflow-hidden">

        <video autoplay disablepictureinpicture loop muted class="w-full h-full absolute object-cover -z-5">
            <source src={`${base}/brand/hero-vid.webm`} type="video/webm" />
        </video>

        <div class="flex flex-col flex-wrap gap-24 justify-center py-16 px-16 md:px-48 h-full z-8">
            <h3 class="h1 leading-[1]">A tool to structure and visualize provenance research</h3>
            <p class="text-brand-contrast-dark">Loupe helps researchers build, visualize, and share the evidence behind an object's history, from its first known record to today.</p>

            <div class="download-desktop hidden md:inline">
	            <a href="https://digitalbenin.org" class="btn preset-filled bg-primary-800 px-32 py-16 gap-8 hover:gap-12">
                    Use it now
                    <IconArrowUpRight class="size-18 transition" stroke="1.5"/>
                </a>
            </div>

            <div class="download-mobile inline md:hidden">
                <Dialog>
	                <Dialog.Trigger class="btn preset-filled bg-primary-800 px-32 py-16 gap-8 hover:gap-12">
                        Use it
                        <IconArrowUpRight class="size-18 transition" stroke="1.5"/>
                    </Dialog.Trigger>
                    <MobileModal />
                </Dialog>
            </div>
        </div>
    </div>
</section>
