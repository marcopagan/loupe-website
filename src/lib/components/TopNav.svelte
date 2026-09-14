<script lang="ts">
    import { IconBook2 } from '@tabler/icons-svelte';
    import { base } from '$app/paths';
    let body: HTMLBodyElement;

    $effect(() => {
        body = document.getElementsByTagName("body")[0];
    });
</script>

<header class="sticky top-0 z-16">
    <div class="container mx-auto flex flex-wrap content-end justify-between px-16 py-8">
        <button class="flex gap-8 pb-8" onclick={() => body.scrollIntoView()}>
            <img src={`${base}/brand/icon-logo.svg`} width="36" height="36" alt="Loupe logo"/>
            <h1 class="h2">Loupe</h1>
        </button>
	
	    <a href="https://wikipedia.org" type="button" class="btn hover:preset-tonal gap-8">
            User Guide <IconBook2 class="size-18" stroke='2'/>
        </a>
    </div>
</header>


<style>
    header{
        background: linear-gradient(var(--color-white), #ffffff00);
    }
</style>